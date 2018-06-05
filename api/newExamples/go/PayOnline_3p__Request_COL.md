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
PayOnLine3p.Psp_MerchTxRef = "ORDER76666-3"
PayOnLine3p.Psp_MerchOrderId = "ORDER76666"
PayOnLine3p.Psp_ReturnURL = "http://localhost/"
PayOnLine3p.Psp_FrmLanguage = "es_AR"
PayOnLine3p.Psp_Amount = "1360000"
PayOnLine3p.Psp_NumPayments = "1"
PayOnLine3p.Psp_Currency = "170"
PayOnLine3p.Psp_Country = "COL"
PayOnLine3p.Psp_Product = "14"
PayOnLine3p.Psp_PosDateTime = "2019-12-01 12:00:00"

pspAmountAdditionalDetails := nps.NewAmountAdditionalDetailsStruct()
pspAmountAdditionalDetails.Tip = "20"
pspAmountAdditionalDetails.Discount = "1"

ComplexElementArray Taxes = new ComplexElementArray();

ComplexElementArrayItem Taxes1 = new ComplexElementArrayItem();
Taxes1.TypeId = "100"
Taxes1.Amount = "200000"

Taxes.add(Taxes1);

ComplexElementArrayItem Taxes2 = new ComplexElementArrayItem();
Taxes2.TypeId = "501"
Taxes2.Amount = "160000"
Taxes2.Rate = "1600"
Taxes2.BaseAmount = "1000000"

Taxes.add(Taxes2);

pspAmountAdditionalDetails.Taxes = Taxes

PayOnLine3p.psp_AmountAdditionalDetails = pspAmountAdditionalDetails

response, err := service.PayOnLine_3p(PayOnLine3p)

if err != nil {
    fmt.Printf("Error: = [%s]", err)
}
fmt.Printf("Response = [%s] [%s]", resp.Psp_ResponseCod, resp.Psp_ResponseMsg)
fmt.Printf("Extended = [%s]", resp.Psp_ResponseExtended)



