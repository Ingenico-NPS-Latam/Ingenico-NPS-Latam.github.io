package main

import (
        "fmt"
        "log"
        "npsSdk"
        CONSTANTS "npsSdk/constants"
)

service:= nps.NewPaymentServicePlatformPortType(true)

Refund := nps.NewRequerimientoStruct_Refund()

Refund.Psp_Version = "2.2"
Refund.Psp_MerchantId = "sdk_test"
Refund.Psp_TxSource = "WEB"
Refund.Psp_MerchTxRef = "ORDER66666-3"
Refund.Psp_TransactionId_Orig = "2693348"
Refund.Psp_AmountToRefund = "15050"
Refund.Psp_UserId = "john_doe"
Refund.Psp_PosDateTime = "2019-12-01 12:00:00"

response, err := service.Refund(Refund)

if err != nil {
    fmt.Printf("Error: = [%s]", err)
}
fmt.Printf("Response = [%s] [%s]", resp.Psp_ResponseCod, resp.Psp_ResponseMsg)
fmt.Printf("Extended = [%s]", resp.Psp_ResponseExtended)



