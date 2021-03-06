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

NotifyFraudScreeningReview := npsSdk.NewRequerimientoStruct_NotifyFraudScreeningReview()

NotifyFraudScreeningReview.Psp_Version = "2.2"
NotifyFraudScreeningReview.Psp_MerchantId = "sdk_test"
NotifyFraudScreeningReview.Psp_Criteria = "T"
NotifyFraudScreeningReview.Psp_CriteriaId = "ORDER69461-3"
NotifyFraudScreeningReview.Psp_ReviewResult = "A"
NotifyFraudScreeningReview.Psp_PosDateTime = "2019-12-01 12:00:00"

resp, err := service.NotifyFraudScreeningReview(NotifyFraudScreeningReview)

if err != nil {
    fmt.Printf("Error: = [%s]", err)
}
fmt.Printf("Response = [%s] [%s]", resp.Psp_ResponseCod, resp.Psp_ResponseMsg)
fmt.Printf("Extended = [%s]", resp.Psp_ResponseExtended)
