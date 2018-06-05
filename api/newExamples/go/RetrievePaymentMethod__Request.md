package main

import (
        "fmt"
        "log"
        "npsSdk"
        CONSTANTS "npsSdk/constants"
)

service:= nps.NewPaymentServicePlatformPortType(true)

RetrievePaymentMethod := nps.NewRequerimientoStruct_RetrievePaymentMethod()

RetrievePaymentMethod.Psp_Version = "2.2"
RetrievePaymentMethod.Psp_MerchantId = "sdk_test"
RetrievePaymentMethod.Psp_PaymentMethodId = "jGW24iDaoMBzfKHViL18TmHo9sHBgW4J"
RetrievePaymentMethod.Psp_PosDateTime = "2008-01-12 13:05:00"

response, err := service.RetrievePaymentMethod(RetrievePaymentMethod)

if err != nil {
    fmt.Printf("Error: = [%s]", err)
}
fmt.Printf("Response = [%s] [%s]", resp.Psp_ResponseCod, resp.Psp_ResponseMsg)
fmt.Printf("Extended = [%s]", resp.Psp_ResponseExtended)



