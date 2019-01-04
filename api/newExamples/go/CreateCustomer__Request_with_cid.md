package main

import (
    "fmt"
    "github.com/Ingenico-NPS-Latam/nps-sdk-go/npsSdk"
    CONSTANTS "github.com/Ingenico-NPS-Latam/nps-sdk-go/npsSdk/constants"
)

func main() {

err := npsSdk.Configure(map[string]interface{}(
    "environment": CONSTANTS.SANDBOX_ENV,
    "secret_key": "_YOUR_SECRET_KEY_",
    "debug": true,
    "log_level": CONSTANTS.DEBUG,
})

service := npsSdk.NewPaymentServicePlatformPortType(true)

CreateCustomer := npsSdk.NewRequerimientoStruct_CreateCustomer()

CreateCustomer.Psp_Version = "2.2"
CreateCustomer.Psp_MerchantId = "sdk_test"
CreateCustomer.Psp_EmailAddress = "jhon.doe@example.com"
CreateCustomer.Psp_AlternativeEmailAddress = "jdoe@example.com"
CreateCustomer.Psp_AccountID = "jdoe78"
CreateCustomer.Psp_AccountCreatedAt = "2010-10-23"

pspPaymentMethod := nps.NewPaymentMethodStruct()

CardInputDetails := nps.NewCardInputDetailsStruct()
CardInputDetails.Number = "4507990000000010"
CardInputDetails.ExpirationDate = "2501"
CardInputDetails.SecurityCode = "123"
CardInputDetails.HolderName = "JOHN DOE"

pspPaymentMethod.CardInputDetails = CardInputDetails

CreateCustomer.psp_PaymentMethod = pspPaymentMethod
CreateCustomer.Psp_PosDateTime = "2008-01-12 13:05:00"

resp, err := service.CreateCustomer(CreateCustomer)

if err != nil {
    fmt.Printf("Error: = [%s]", err)
}
fmt.Printf("Response = [%s] [%s]", resp.Psp_ResponseCod, resp.Psp_ResponseMsg)
fmt.Printf("Extended = [%s]", resp.Psp_ResponseExtended)
