package main

import (
        "fmt"
        "log"
        "npsSdk"
        CONSTANTS "npsSdk/constants"
)

service:= nps.NewPaymentServicePlatformPortType(true)

Capture := nps.NewRequerimientoStruct_Capture()

Capture.Psp_Version = "2.2"
Capture.Psp_MerchantId = "sdk_test"
Capture.Psp_TxSource = "WEB"
Capture.Psp_MerchTxRef = "ORDER66666-3"
Capture.Psp_TransactionId_Orig = "2693348"
Capture.Psp_AmountToCapture = "15050"
Capture.Psp_UserId = "john_doe"
Capture.Psp_PosDateTime = "2019-12-01 12:00:00"

response, err := service.Capture(Capture)

if err != nil {
    fmt.Printf("Error: = [%s]", err)
}
fmt.Printf("Response = [%s] [%s]", resp.Psp_ResponseCod, resp.Psp_ResponseMsg)
fmt.Printf("Extended = [%s]", resp.Psp_ResponseExtended)



