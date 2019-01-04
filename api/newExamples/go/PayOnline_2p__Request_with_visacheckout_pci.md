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

PayOnLine2p := npsSdk.NewRequerimientoStruct_PayOnLine_2p()

PayOnLine2p.Psp_Version = "2.2"
PayOnLine2p.Psp_MerchantId = "sdk_test"
PayOnLine2p.Psp_TxSource = "WEB"
PayOnLine2p.Psp_MerchTxRef = "ORDER69461-3"
PayOnLine2p.Psp_MerchOrderId = "ORDER69461"
PayOnLine2p.Psp_Amount = "15050"
PayOnLine2p.Psp_NumPayments = "1"
PayOnLine2p.Psp_Currency = "032"
PayOnLine2p.Psp_Country = "ARG"
PayOnLine2p.Psp_Product = "14"
PayOnLine2p.Psp_CardNumber = "4507990000000010"
PayOnLine2p.Psp_CardExpDate = "1912"
PayOnLine2p.Psp_CardSecurityCode = "325"
PayOnLine2p.Psp_PosDateTime = "2019-12-01 12:00:00"

pspWalletReference := nps.NewWalletReferenceStruct()
pspWalletReference.WalletTypeId = "1"

PayOnLine2p.psp_WalletReference = pspWalletReference

resp, err := service.PayOnLine_2p(PayOnLine2p)

if err != nil {
    fmt.Printf("Error: = [%s]", err)
}
fmt.Printf("Response = [%s] [%s]", resp.Psp_ResponseCod, resp.Psp_ResponseMsg)
fmt.Printf("Extended = [%s]", resp.Psp_ResponseExtended)
