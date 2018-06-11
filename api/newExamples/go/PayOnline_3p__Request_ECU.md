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
PayOnLine3p.Psp_MerchantId = "psp_test"
PayOnLine3p.Psp_TxSource = "WEB"
PayOnLine3p.Psp_MerchTxRef = "ORDER76666-3"
PayOnLine3p.Psp_MerchOrderId = "ORDER76666"
PayOnLine3p.Psp_ReturnURL = "http://localhost/"
PayOnLine3p.Psp_FrmLanguage = "es_AR"
PayOnLine3p.Psp_NumPayments = "1"
PayOnLine3p.Psp_Currency = "840"
PayOnLine3p.Psp_Country = "ECU"
PayOnLine3p.Psp_Product = "14"
PayOnLine3p.Psp_PosDateTime = "2019-12-01 12:00:00"
PayOnLine3p.Psp_Amount = "31200"

pspAmountAdditionalDetails := nps.NewAmountAdditionalDetailsStruct()

ComplexElementArray Taxes = new ComplexElementArray();

ComplexElementArrayItem Taxes1 = new ComplexElementArrayItem();
Taxes1.TypeId = "700"
Taxes1.Amount = "1200"
Taxes1.Rate = "1200"
Taxes1.BaseAmount = "100000"

Taxes.add(Taxes1);

ComplexElementArrayItem Taxes2 = new ComplexElementArrayItem();
Taxes2.TypeId = "701"
Taxes2.BaseAmount = "20000"

Taxes.add(Taxes2);

pspAmountAdditionalDetails.Taxes = Taxes

PayOnLine3p.psp_AmountAdditionalDetails = pspAmountAdditionalDetails

response, err := service.PayOnLine_3p(PayOnLine3p)

if err != nil {
    fmt.Printf("Error: = [%s]", err)
}
fmt.Printf("Response = [%s] [%s]", resp.Psp_ResponseCod, resp.Psp_ResponseMsg)
fmt.Printf("Extended = [%s]", resp.Psp_ResponseExtended)



