package main

import (
        "fmt"
        "log"
        "npsSdk"
        CONSTANTS "npsSdk/constants"
)

service:= nps.NewPaymentServicePlatformPortType(true)

RecachePaymentMethodToken := nps.NewRequerimientoStruct_RecachePaymentMethodToken()

RecachePaymentMethodToken.Psp_Version = "2.2"
RecachePaymentMethodToken.Psp_MerchantId = "sdk_test"
RecachePaymentMethodToken.Psp_PaymentMethodId = "Nzmd7DyGytXXC5PtKwnCsXXuQWHJB9EE"
RecachePaymentMethodToken.Psp_CardSecurityCode = "123"
RecachePaymentMethodToken.Psp_ClientSession = "C5jwwbyAYneLbvZe0IYPHTvn7ODMb3vG8ZqCYaYIioUmWUbcgKscGpg8WhXrspRs"

response, err := service.RecachePaymentMethodToken(RecachePaymentMethodToken)

if err != nil {
    fmt.Printf("Error: = [%s]", err)
}
fmt.Printf("Response = [%s] [%s]", resp.Psp_ResponseCod, resp.Psp_ResponseMsg)
fmt.Printf("Extended = [%s]", resp.Psp_ResponseExtended)



