package main

import (
        "fmt"
        "log"
        "npsSdk"
        CONSTANTS "npsSdk/constants"
)

service:= nps.NewPaymentServicePlatformPortType(true)

CreatePaymentMethodToken := nps.NewRequerimientoStruct_CreatePaymentMethodToken()

CreatePaymentMethodToken.Psp_Version = "2.2"
CreatePaymentMethodToken.Psp_MerchantId = "sdk_test"

pspCardInputDetails := nps.NewCardInputDetailsStruct()
pspCardInputDetails.Number = "4507990000000010"
pspCardInputDetails.ExpirationDate = "2501"
pspCardInputDetails.SecurityCode = "123"
pspCardInputDetails.HolderName = "JOHN DOE"

CreatePaymentMethodToken.psp_CardInputDetails = pspCardInputDetails
CreatePaymentMethodToken.Psp_ClientSession = "C5jwwbyAYneLbvZe0IYPHTvn7ODMb3vG8ZqCYaYIioUmWUbcgKscGpg8WhXrspRs"

response, err := service.CreatePaymentMethodToken(CreatePaymentMethodToken)

if err != nil {
    fmt.Printf("Error: = [%s]", err)
}
fmt.Printf("Response = [%s] [%s]", resp.Psp_ResponseCod, resp.Psp_ResponseMsg)
fmt.Printf("Extended = [%s]", resp.Psp_ResponseExtended)



