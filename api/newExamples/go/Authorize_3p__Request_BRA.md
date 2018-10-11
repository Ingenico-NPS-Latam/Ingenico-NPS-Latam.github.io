package main

import (
        "fmt"
        "log"
        "npsSdk"
        CONSTANTS "npsSdk/constants"
)

service:= nps.NewPaymentServicePlatformPortType(true)

Authorize3p := nps.NewRequerimientoStruct_Authorize_3p()

Authorize3p.Psp_Version = "2.2"
Authorize3p.Psp_MerchantId = "sdk_test"
Authorize3p.Psp_TxSource = "WEB"
Authorize3p.Psp_MerchTxRef = "ORDER76666-3"
Authorize3p.Psp_MerchOrderId = "ORDER76666"
Authorize3p.Psp_ReturnURL = "http://localhost/"
Authorize3p.Psp_FrmLanguage = "es_AR"
Authorize3p.Psp_Amount = "1200000"
Authorize3p.Psp_NumPayments = "1"
Authorize3p.Psp_Currency = "986"
Authorize3p.Psp_Country = "BRA"
Authorize3p.Psp_Product = "14"
Authorize3p.Psp_PosDateTime = "2019-12-01 12:00:00"

pspAmountAdditionalDetails := nps.NewAmountAdditionalDetailsRequestStruct()
pspAmountAdditionalDetails.Tip = "20"
pspAmountAdditionalDetails.Discount = "1"

Taxes := nps.NewArrayOf_TaxesRequestStruct()
Taxes.Items = make([]*nps.NewTaxesRequestStruct(), 0)

Taxes1 := nps.NewTaxesRequestStruct()
Taxes1.TypeId = "100"
Taxes1.Amount = "200000"

Taxes.Items = append(Taxes.Items, Taxes1)

Authorize3p.psp_AmountAdditionalDetails = pspAmountAdditionalDetails

response, err := service.Authorize_3p(Authorize3p)

if err != nil {
    fmt.Printf("Error: = [%s]", err)
}
fmt.Printf("Response = [%s] [%s]", resp.Psp_ResponseCod, resp.Psp_ResponseMsg)
fmt.Printf("Extended = [%s]", resp.Psp_ResponseExtended)



