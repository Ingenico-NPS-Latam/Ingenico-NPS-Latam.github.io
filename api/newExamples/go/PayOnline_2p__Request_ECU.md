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
PayOnLine2p.Psp_NumPayments = "1"
PayOnLine2p.Psp_Currency = "840"
PayOnLine2p.Psp_Country = "ECU"
PayOnLine2p.Psp_Product = "1"
PayOnLine2p.Psp_CardNumber = "376650002408696"
PayOnLine2p.Psp_CardExpDate = "1808"
PayOnLine2p.Psp_PosDateTime = "2018-07-05 12:00:00"
PayOnLine2p.Psp_Amount = "31200"

pspAmountAdditionalDetails := nps.NewAmountAdditionalDetailsStruct()

Taxes := nps.NewTaxesStruct()

Taxes1 := Taxes.Items[1];
Taxes1.TypeId = "700"
Taxes1.Amount = "1200"
Taxes1.Rate = "1200"
Taxes1.BaseAmount = "10000"

Taxes2 := Taxes.Items[2];
Taxes2.TypeId = "701"
Taxes2.BaseAmount = "20000"


pspAmountAdditionalDetails.Taxes = Taxes

PayOnLine2p.psp_AmountAdditionalDetails = pspAmountAdditionalDetails

response, err := service.PayOnLine_2p(PayOnLine2p)

if err != nil {
    fmt.Printf("Error: = [%s]", err)
}
fmt.Printf("Response = [%s] [%s]", resp.Psp_ResponseCod, resp.Psp_ResponseMsg)
fmt.Printf("Extended = [%s]", resp.Psp_ResponseExtended)



