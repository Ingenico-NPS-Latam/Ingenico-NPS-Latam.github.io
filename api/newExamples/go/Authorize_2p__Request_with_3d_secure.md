package main

import (
        "fmt"
        "log"
        "npsSdk"
        CONSTANTS "npsSdk/constants"
)

service:= nps.NewPaymentServicePlatformPortType(true)

Authorize2p := nps.NewRequerimientoStruct_Authorize_2p()

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

response, err := service.Authorize_2p(Authorize2p)

if err != nil {
    fmt.Printf("Error: = [%s]", err)
}
fmt.Printf("Response = [%s] [%s]", resp.Psp_ResponseCod, resp.Psp_ResponseMsg)
fmt.Printf("Extended = [%s]", resp.Psp_ResponseExtended)



