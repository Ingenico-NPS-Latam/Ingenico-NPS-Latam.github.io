package main

import (
        "fmt"
        "log"
        "npsSdk"
        CONSTANTS "npsSdk/constants"
)

service:= nps.NewPaymentServicePlatformPortType(true)

UpdatePaymentMethod := nps.NewRequerimientoStruct_UpdatePaymentMethod()

UpdatePaymentMethod.Psp_Version = "2.2"
UpdatePaymentMethod.Psp_MerchantId = "sdk_test"
UpdatePaymentMethod.Psp_PaymentMethodId = "Nzmd7DyGytXXC5PtKwnCsXXuQWHJB9EE"
UpdatePaymentMethod.Psp_PaymentMethodTag = "Corporate card"

pspCardInputDetails := nps.NewCardInputDetailsStruct()
pspCardInputDetails.ExpirationDate = "2501"

UpdatePaymentMethod.psp_CardInputDetails = pspCardInputDetails
UpdatePaymentMethod.Psp_PosDateTime = "2008-01-12 13:05:00"

response, err := service.UpdatePaymentMethod(UpdatePaymentMethod)

if err != nil {
    fmt.Printf("Error: = [%s]", err)
}
fmt.Printf("Response = [%s] [%s]", resp.Psp_ResponseCod, resp.Psp_ResponseMsg)
fmt.Printf("Extended = [%s]", resp.Psp_ResponseExtended)



