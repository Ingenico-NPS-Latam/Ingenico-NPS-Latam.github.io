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

pspAmountAdditionalDetails := nps.NewAmountAdditionalDetailsStruct()
pspAmountAdditionalDetails.Tip = "20"
pspAmountAdditionalDetails.Discount = "1"

Taxes := nps.NewTaxesStruct()

Taxes1 := Taxes.Items[1];
Taxes1.TypeId = "100"
Taxes1.Amount = "200000"


pspAmountAdditionalDetails.Taxes = Taxes

Authorize3p.psp_AmountAdditionalDetails = pspAmountAdditionalDetails

response, err := service.Authorize_3p(Authorize3p)

if err != nil {
    fmt.Printf("Error: = [%s]", err)
}
fmt.Printf("Response = [%s] [%s]", resp.Psp_ResponseCod, resp.Psp_ResponseMsg)
fmt.Printf("Extended = [%s]", resp.Psp_ResponseExtended)



