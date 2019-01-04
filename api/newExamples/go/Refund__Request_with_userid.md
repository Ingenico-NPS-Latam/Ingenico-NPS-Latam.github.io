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

Refund := npsSdk.NewRequerimientoStruct_Refund()

Refund.Psp_Version = "2.2"
Refund.Psp_MerchantId = "sdk_test"
Refund.Psp_TxSource = "WEB"
Refund.Psp_MerchTxRef = "ORDER66666-3"
Refund.Psp_TransactionId_Orig = "2693348"
Refund.Psp_AmountToRefund = "15050"
Refund.Psp_UserId = "john_doe"
Refund.Psp_PosDateTime = "2019-12-01 12:00:00"

resp, err := service.Refund(Refund)

if err != nil {
    fmt.Printf("Error: = [%s]", err)
}
fmt.Printf("Response = [%s] [%s]", resp.Psp_ResponseCod, resp.Psp_ResponseMsg)
fmt.Printf("Extended = [%s]", resp.Psp_ResponseExtended)
