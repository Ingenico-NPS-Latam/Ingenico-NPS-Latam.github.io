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
PayOnLine2p.Psp_MerchantId = "psp_test"
PayOnLine2p.Psp_TxSource = "WEB"
PayOnLine2p.Psp_MerchTxRef = "ORDERX1466Xz-3"
PayOnLine2p.Psp_MerchOrderId = "ORDERX1466Xz"
PayOnLine2p.Psp_Amount = "1200000"
PayOnLine2p.Psp_NumPayments = "3"
PayOnLine2p.Psp_CardSecurityCode = "321"
PayOnLine2p.Psp_Currency = "986"
PayOnLine2p.Psp_Country = "BRA"
PayOnLine2p.Psp_Product = "5"
PayOnLine2p.Psp_Plan = "CC"
PayOnLine2p.Psp_CardNumber = "5453010000083303"
PayOnLine2p.Psp_CardExpDate = "1904"
PayOnLine2p.Psp_PosDateTime = "2017-03-31 16:14:06"
PayOnLine2p.Psp_ForceProcessingMethod = "16"

pspAmountAdditionalDetails := nps.NewAmountAdditionalDetailsStruct()
pspAmountAdditionalDetails.Tip = "20"
pspAmountAdditionalDetails.Discount = "1"

Taxes := nps.NewTaxesStruct()

Taxes1 := Taxes.Items[1];
Taxes1.TypeId = "100"
Taxes1.Amount = "200000"


pspAmountAdditionalDetails.Taxes = Taxes

PayOnLine2p.psp_AmountAdditionalDetails = pspAmountAdditionalDetails

response, err := service.PayOnLine_2p(PayOnLine2p)

if err != nil {
    fmt.Printf("Error: = [%s]", err)
}
fmt.Printf("Response = [%s] [%s]", resp.Psp_ResponseCod, resp.Psp_ResponseMsg)
fmt.Printf("Extended = [%s]", resp.Psp_ResponseExtended)



