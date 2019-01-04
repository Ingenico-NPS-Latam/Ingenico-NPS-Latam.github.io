package main

import (
    "fmt"
    "github.com/Ingenico-NPS-Latam/nps-sdk-go/npsSdk"
    CONSTANTS "github.com/Ingenico-NPS-Latam/nps-sdk-go/npsSdk/constants"
)

func main() {

err := npsSdk.Configure(map[string]interface{}(
    "environment": CONSTANTS.SANDBOX_ENV,
    "secret_key": "_YOUR_SECRET_KEY_",
    "debug": true,
    "log_level": CONSTANTS.DEBUG,
})

service := npsSdk.NewPaymentServicePlatformPortType(true)

Capture := npsSdk.NewRequerimientoStruct_Capture()

Capture.Psp_Version = "2.2"
Capture.Psp_MerchantId = "sdk_test"
Capture.Psp_TxSource = "WEB"
Capture.Psp_MerchTxRef = "ORDER66666-3"
Capture.Psp_TransactionId_Orig = "2693348"
Capture.Psp_AmountToCapture = "15050"
Capture.Psp_UserId = "john_doe"
Capture.Psp_PosDateTime = "2019-12-01 12:00:00"

resp, err := service.Capture(Capture)

if err != nil {
    fmt.Printf("Error: = [%s]", err)
}
fmt.Printf("Response = [%s] [%s]", resp.Psp_ResponseCod, resp.Psp_ResponseMsg)
fmt.Printf("Extended = [%s]", resp.Psp_ResponseExtended)
