package main

import (
        "fmt"
        "log"
        "npsSdk"
        CONSTANTS "npsSdk/constants"
)

service:= nps.NewPaymentServicePlatformPortType(true)

DeletePaymentMethod := nps.NewRequerimientoStruct_DeletePaymentMethod()

DeletePaymentMethod.Psp_Version = "2.2"
DeletePaymentMethod.Psp_MerchantId = "sdk_test"
DeletePaymentMethod.Psp_PaymentMethodId = "Nzmd7DyGytXXC5PtKwnCsXXuQWHJB9EE"
DeletePaymentMethod.Psp_PosDateTime = "2008-01-12 13:05:00"

response, err := service.DeletePaymentMethod(DeletePaymentMethod)

if err != nil {
    fmt.Printf("Error: = [%s]", err)
}
fmt.Printf("Response = [%s] [%s]", resp.Psp_ResponseCod, resp.Psp_ResponseMsg)
fmt.Printf("Extended = [%s]", resp.Psp_ResponseExtended)



