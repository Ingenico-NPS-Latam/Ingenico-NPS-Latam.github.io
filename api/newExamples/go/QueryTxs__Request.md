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

QueryTxs := npsSdk.NewRequerimientoStruct_QueryTxs()

QueryTxs.Psp_Version = "2.2"
QueryTxs.Psp_MerchantId = "sdk_test"
QueryTxs.Psp_QueryCriteria = "O"
QueryTxs.Psp_QueryCriteriaId = "ORDER69461-3"
QueryTxs.Psp_PosDateTime = "2019-12-01 12:00:00"

resp, err := service.QueryTxs(QueryTxs)

if err != nil {
    fmt.Printf("Error: = [%s]", err)
}
fmt.Printf("Response = [%s] [%s]", resp.Psp_ResponseCod, resp.Psp_ResponseMsg)
fmt.Printf("Extended = [%s]", resp.Psp_ResponseExtended)
