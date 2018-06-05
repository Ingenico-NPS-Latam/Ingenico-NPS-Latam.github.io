package main

import (
        "fmt"
        "log"
        "npsSdk"
        CONSTANTS "npsSdk/constants"
)

service:= nps.NewPaymentServicePlatformPortType(true)

PayOnLine3p := nps.NewRequerimientoStruct_PayOnLine_3p()

PayOnLine3p.Psp_Version = "2.2"
PayOnLine3p.Psp_MerchantId = "sdk_test"
PayOnLine3p.Psp_TxSource = "WEB"
PayOnLine3p.Psp_MerchTxRef = "ORDER66666-3"
PayOnLine3p.Psp_MerchOrderId = "ORDER66666"
PayOnLine3p.Psp_ReturnURL = "http://localhost/"
PayOnLine3p.Psp_FrmLanguage = "es_AR"
PayOnLine3p.Psp_Amount = "15050"
PayOnLine3p.Psp_NumPayments = "1"
PayOnLine3p.Psp_Currency = "032"
PayOnLine3p.Psp_Country = "ARG"
PayOnLine3p.Psp_Product = "14"

pspVaultReference := nps.NewVaultReferenceStruct()
pspVaultReference.CustomerId = "K8sj5rBrGqPBczTR4LtuKE6g4iZMmY9f"

PayOnLine3p.psp_VaultReference = pspVaultReference
PayOnLine3p.Psp_PosDateTime = "2019-12-01 12:00:00"

response, err := service.PayOnLine_3p(PayOnLine3p)

if err != nil {
    fmt.Printf("Error: = [%s]", err)
}
fmt.Printf("Response = [%s] [%s]", resp.Psp_ResponseCod, resp.Psp_ResponseMsg)
fmt.Printf("Extended = [%s]", resp.Psp_ResponseExtended)



