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

Authorize3p := npsSdk.NewRequerimientoStruct_Authorize_3p()

Authorize3p.Psp_Version = "2.2"
Authorize3p.Psp_MerchantId = "sdk_test"
Authorize3p.Psp_TxSource = "WEB"
Authorize3p.Psp_MerchTxRef = "ORDER76666-3"
Authorize3p.Psp_MerchOrderId = "ORDER76666"
Authorize3p.Psp_NumPayments = "1"
Authorize3p.Psp_ReturnURL = "http://localhost/"
Authorize3p.Psp_FrmLanguage = "es_AR"
Authorize3p.Psp_Amount = "15050"
Authorize3p.Psp_Currency = "032"
Authorize3p.Psp_Country = "ARG"
Authorize3p.Psp_Product = "14"
Authorize3p.Psp_PosDateTime = "2019-12-01 12:00:00"

resp, err := service.Authorize_3p(Authorize3p)

if err != nil {
    fmt.Printf("Error: = [%s]", err)
}
fmt.Printf("Response = [%s] [%s]", resp.Psp_ResponseCod, resp.Psp_ResponseMsg)
fmt.Printf("Extended = [%s]", resp.Psp_ResponseExtended)
