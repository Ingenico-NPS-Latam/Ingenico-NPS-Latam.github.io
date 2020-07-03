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

Authorize2p := npsSdk.NewRequerimientoStruct_Authorize_2p()

Authorize2p.Psp_Version = "2.2"
Authorize2p.Psp_MerchantId = "sdk_test"
Authorize2p.Psp_TxSource = "WEB"
Authorize2p.Psp_MerchTxRef = "ORDERX1466Xz-3"
Authorize2p.Psp_MerchOrderId = "ORDERX1466Xz"
Authorize2p.Psp_Amount = "15050"
Authorize2p.Psp_NumPayments = "1"
Authorize2p.Psp_Currency = "032"
Authorize2p.Psp_Country = "ARG"
Authorize2p.Psp_Product = "14"
Authorize2p.Psp_CardNumber = "4507990000000010"
Authorize2p.Psp_CardExpDate = "1912"
Authorize2p.Psp_PosDateTime = "2019-12-01 12:00:00"
Authorize2p.Psp_3dSecure_XID = "MjY0MjAxNjA4MDIyMDUzMzYyNjU="
Authorize2p.Psp_3dSecure_CAVV = "AAABBYZ3N5Qhl3kBU3c3ELGUsMY="
Authorize2p.Psp_3dSecure_ECI = "05"
Authorize2p.Psp_3dSecure_Secured = "1"
Authorize2p.psp_3dSecure_ProtocolVersion = "2.1.0"
Authorize2p.psp_3dSecure_DirectoryServerTransactionId = "c4e59ceb-a382-4d6a-bc87-385d591fa09d"

resp, err := service.Authorize_2p(Authorize2p)

if err != nil {
    fmt.Printf("Error: = [%s]", err)
}
fmt.Printf("Response = [%s] [%s]", resp.Psp_ResponseCod, resp.Psp_ResponseMsg)
fmt.Printf("Extended = [%s]", resp.Psp_ResponseExtended)
