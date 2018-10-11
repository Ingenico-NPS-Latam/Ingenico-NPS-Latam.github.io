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
PayOnLine2p.Psp_Amount = "1360000"
PayOnLine2p.Psp_NumPayments = "1"
PayOnLine2p.Psp_Currency = "170"
PayOnLine2p.Psp_Country = "COL"
PayOnLine2p.Psp_Product = "14"
PayOnLine2p.Psp_CardNumber = "4005580000050003"
PayOnLine2p.Psp_CardExpDate = "1812"
PayOnLine2p.Psp_PosDateTime = "2019-12-01 12:00:00"

pspAmountAdditionalDetails := nps.NewAmountAdditionalDetailsRequestStruct()
pspAmountAdditionalDetails.Tip = "20"
pspAmountAdditionalDetails.Discount = "1"

Taxes := nps.NewArrayOf_TaxesRequestStruct()
Taxes.Items = make([]*nps.NewTaxesRequestStruct(), 0)

Taxes1 := nps.NewTaxesRequestStruct()
Taxes1.TypeId = "100"
Taxes1.Amount = "200000"

Taxes.Items = append(Taxes.Items, Taxes1)
Taxes2 := nps.NewTaxesRequestStruct()
Taxes2.TypeId = "501"
Taxes2.Amount = "160000"
Taxes2.Rate = "1600"
Taxes2.BaseAmount = "1000000"

Taxes.Items = append(Taxes.Items, Taxes2)

PayOnLine2p.psp_AmountAdditionalDetails = pspAmountAdditionalDetails

response, err := service.PayOnLine_2p(PayOnLine2p)

if err != nil {
    fmt.Printf("Error: = [%s]", err)
}
fmt.Printf("Response = [%s] [%s]", resp.Psp_ResponseCod, resp.Psp_ResponseMsg)
fmt.Printf("Extended = [%s]", resp.Psp_ResponseExtended)



