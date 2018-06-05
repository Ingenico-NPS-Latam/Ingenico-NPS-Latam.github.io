package main

import (
        "fmt"
        "log"
        "npsSdk"
        CONSTANTS "npsSdk/constants"
)

service:= nps.NewPaymentServicePlatformPortType(true)

RetrievePaymentMethodToken := nps.NewRequerimientoStruct_RetrievePaymentMethodToken()

RetrievePaymentMethodToken.Psp_Version = "2.2"
RetrievePaymentMethodToken.Psp_MerchantId = "sdk_test"
RetrievePaymentMethodToken.Psp_PaymentMethodToken = "KCVMXsbue5fUKOoAxvp1PTJ94gxv2dQM"
RetrievePaymentMethodToken.Psp_ClientSession = "C5jwwbyAYneLbvZe0IYPHTvn7ODMb3vG8ZqCYaYIioUmWUbcgKscGpg8WhXrspRs"

response, err := service.RetrievePaymentMethodToken(RetrievePaymentMethodToken)

if err != nil {
    fmt.Printf("Error: = [%s]", err)
}
fmt.Printf("Response = [%s] [%s]", resp.Psp_ResponseCod, resp.Psp_ResponseMsg)
fmt.Printf("Extended = [%s]", resp.Psp_ResponseExtended)



