package main

import (
        "fmt"
        "log"
        "npsSdk"
        CONSTANTS "npsSdk/constants"
)

service:= nps.NewPaymentServicePlatformPortType(true)

UpdateCustomer := nps.NewRequerimientoStruct_UpdateCustomer()

UpdateCustomer.Psp_Version = "2.2"
UpdateCustomer.Psp_MerchantId = "sdk_test"
UpdateCustomer.Psp_CustomerId = "bMnVPbNgX55oUz1VLgC41E5iD2rYRo2b"
UpdateCustomer.Psp_EmailAddress = "jhon.doe@example.com"
UpdateCustomer.Psp_AlternativeEmailAddress = "jdoe@example.com"
UpdateCustomer.Psp_AccountCreatedAt = "2010-10-23"
UpdateCustomer.Psp_AccountID = "jdoe78"

pspPaymentMethod := nps.NewPaymentMethodStruct()

CardInputDetails := nps.NewCardInputDetailsStruct()
CardInputDetails.Number = "4507990000000010"
CardInputDetails.ExpirationDate = "2501"
CardInputDetails.SecurityCode = "123"
CardInputDetails.HolderName = "JOHN DOE"

pspPaymentMethod.CardInputDetails = CardInputDetails

UpdateCustomer.psp_PaymentMethod = pspPaymentMethod
UpdateCustomer.Psp_PosDateTime = "2008-01-12 13:05:00"

response, err := service.UpdateCustomer(UpdateCustomer)

if err != nil {
    fmt.Printf("Error: = [%s]", err)
}
fmt.Printf("Response = [%s] [%s]", resp.Psp_ResponseCod, resp.Psp_ResponseMsg)
fmt.Printf("Extended = [%s]", resp.Psp_ResponseExtended)



