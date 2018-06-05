package main

import (
        "fmt"
        "log"
        "npsSdk"
        CONSTANTS "npsSdk/constants"
)

service:= nps.NewPaymentServicePlatformPortType(true)

CreatePaymentMethodFromPayment := nps.NewRequerimientoStruct_CreatePaymentMethodFromPayment()

CreatePaymentMethodFromPayment.Psp_Version = "2.2"
CreatePaymentMethodFromPayment.Psp_MerchantId = "sdk_test"
CreatePaymentMethodFromPayment.Psp_TransactionId = "65340022"
CreatePaymentMethodFromPayment.Psp_PaymentMethodTag = "Corporate card"
CreatePaymentMethodFromPayment.Psp_PosDateTime = "2008-01-12 13:05:00"

response, err := service.CreatePaymentMethodFromPayment(CreatePaymentMethodFromPayment)

if err != nil {
    fmt.Printf("Error: = [%s]", err)
}
fmt.Printf("Response = [%s] [%s]", resp.Psp_ResponseCod, resp.Psp_ResponseMsg)
fmt.Printf("Extended = [%s]", resp.Psp_ResponseExtended)



