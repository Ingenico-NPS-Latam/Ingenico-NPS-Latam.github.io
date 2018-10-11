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
Authorize2p.Psp_MerchantId = "psp_test"
Authorize2p.Psp_TxSource = "WEB"
Authorize2p.Psp_MerchTxRef = "ORDERX1466Xz-3"
Authorize2p.Psp_MerchOrderId = "ORDERX1466Xz"
Authorize2p.Psp_Amount = "1200000"
Authorize2p.Psp_NumPayments = "3"
Authorize2p.Psp_CardSecurityCode = "321"
Authorize2p.Psp_Currency = "986"
Authorize2p.Psp_Country = "BRA"
Authorize2p.Psp_Product = "5"
Authorize2p.Psp_Plan = "CC"
Authorize2p.Psp_CardNumber = "5453010000083303"
Authorize2p.Psp_CardExpDate = "1904"
Authorize2p.Psp_PosDateTime = "2017-03-31 16:14:06"
Authorize2p.Psp_ForceProcessingMethod = "16"

pspAmountAdditionalDetails := nps.NewAmountAdditionalDetailsRequestStruct()
pspAmountAdditionalDetails.Tip = "20"
pspAmountAdditionalDetails.Discount = "1"

Taxes := nps.NewArrayOf_TaxesRequestStruct()
Taxes.Items = make([]*nps.NewTaxesRequestStruct(), 0)

Taxes1 := nps.NewTaxesRequestStruct()
Taxes1.TypeId = "100"
Taxes1.Amount = "200000"

Taxes.Items = append(Taxes.Items, Taxes1)

Authorize2p.psp_AmountAdditionalDetails = pspAmountAdditionalDetails

response, err := service.Authorize_2p(Authorize2p)

if err != nil {
    fmt.Printf("Error: = [%s]", err)
}
fmt.Printf("Response = [%s] [%s]", resp.Psp_ResponseCod, resp.Psp_ResponseMsg)
fmt.Printf("Extended = [%s]", resp.Psp_ResponseExtended)



