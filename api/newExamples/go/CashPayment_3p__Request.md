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

CashPayment3p := npsSdk.NewRequerimientoStruct_CashPayment_3p()

CashPayment3p.Psp_Version = "2.2"
CashPayment3p.Psp_MerchantId = "sdk_test"
CashPayment3p.Psp_TxSource = "WEB"
CashPayment3p.Psp_MerchTxRef = "ORDER32145-3"
CashPayment3p.Psp_MerchOrderId = "ORDER32145"
CashPayment3p.Psp_ReturnURL = "http://localhost/"
CashPayment3p.Psp_FrmLanguage = "es_AR"
CashPayment3p.Psp_Amount = "15050"
CashPayment3p.Psp_Currency = "032"
CashPayment3p.Psp_Country = "ARG"
CashPayment3p.Psp_Product = "301"
CashPayment3p.Psp_PosDateTime = "2019-12-01 12:00:00"
CashPayment3p.Psp_FirstExpDate = "2020-01-01"

resp, err := service.CashPayment_3p(CashPayment3p)

if err != nil {
    fmt.Printf("Error: = [%s]", err)
}
fmt.Printf("Response = [%s] [%s]", resp.Psp_ResponseCod, resp.Psp_ResponseMsg)
fmt.Printf("Extended = [%s]", resp.Psp_ResponseExtended)
