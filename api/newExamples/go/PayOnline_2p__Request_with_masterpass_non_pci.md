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
PayOnLine2p.Psp_MerchTxRef = "ORDERX1466Xz-3"
PayOnLine2p.Psp_MerchOrderId = "ORDERX1466Xz"
PayOnLine2p.Psp_Amount = "15050"
PayOnLine2p.Psp_NumPayments = "1"
PayOnLine2p.Psp_Currency = "032"
PayOnLine2p.Psp_Country = "ARG"
PayOnLine2p.Psp_Product = "5"
PayOnLine2p.Psp_PosDateTime = "2019-12-01 12:00:00"

pspVaultReference := nps.NewVaultReferenceStruct()
pspVaultReference.PaymentMethodToken = "Nzmd7DyGytXXC5PtKwnCsXXuQWHJB9EE"

PayOnLine2p.psp_VaultReference = pspVaultReference

response, err := service.PayOnLine_2p(PayOnLine2p)

if err != nil {
    fmt.Printf("Error: = [%s]", err)
}
fmt.Printf("Response = [%s] [%s]", resp.Psp_ResponseCod, resp.Psp_ResponseMsg)
fmt.Printf("Extended = [%s]", resp.Psp_ResponseExtended)



