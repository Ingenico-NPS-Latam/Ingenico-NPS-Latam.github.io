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
PayOnLine2p.Psp_3dSecure_XID = "MjY0MjAxNjA4MDIyMDUzMzYyNjU="
PayOnLine2p.Psp_3dSecure_CAVV = "AAABBYZ3N5Qhl3kBU3c3ELGUsMY="
PayOnLine2p.Psp_3dSecure_ECI = "05"
PayOnLine2p.Psp_3dSecure_Secured = "1"
PayOnLine2p.psp_3dSecure_ProtocolVersion = "2.1.0"
PayOnLine2p.psp_3dSecure_DirectoryServerTransactionId = "c4e59ceb-a382-4d6a-bc87-385d591fa09d"

resp, err := service.PayOnLine_2p(PayOnLine2p)

if err != nil {
    fmt.Printf("Error: = [%s]", err)
}
fmt.Printf("Response = [%s] [%s]", resp.Psp_ResponseCod, resp.Psp_ResponseMsg)
fmt.Printf("Extended = [%s]", resp.Psp_ResponseExtended)
