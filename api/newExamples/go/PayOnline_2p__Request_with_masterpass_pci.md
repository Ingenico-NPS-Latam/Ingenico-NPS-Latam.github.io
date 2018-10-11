package main

import (
        "fmt"
        "log"
        "npsSdk"
        CONSTANTS "npsSdk/constants"
)

service:= nps.NewPaymentServicePlatformPortType(true)

PayOnLine2p := nps.NewRequerimientoStruct_PayOnLine_2p()

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
pspWalletReference.WalletTypeId = "2"
pspWalletReference.WalletIdentificationCode = "101"

PayOnLine2p.psp_WalletReference = pspWalletReference

response, err := service.PayOnLine_2p(PayOnLine2p)

if err != nil {
    fmt.Printf("Error: = [%s]", err)
}
fmt.Printf("Response = [%s] [%s]", resp.Psp_ResponseCod, resp.Psp_ResponseMsg)
fmt.Printf("Extended = [%s]", resp.Psp_ResponseExtended)



