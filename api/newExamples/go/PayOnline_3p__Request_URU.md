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
PayOnLine3p.Psp_Amount = "1220000"
PayOnLine3p.Psp_NumPayments = "1"
PayOnLine3p.Psp_Currency = "858"
PayOnLine3p.Psp_Country = "URY"
PayOnLine3p.Psp_Product = "5"
PayOnLine3p.Psp_PosDateTime = "2019-12-01 12:00:00"

pspAmountAdditionalDetails := nps.NewAmountAdditionalDetailsStruct()
pspAmountAdditionalDetails.Tip = "20"
pspAmountAdditionalDetails.Discount = "1"

ComplexElementArray Taxes = new ComplexElementArray();

ComplexElementArrayItem Taxes1 = new ComplexElementArrayItem();
Taxes1.TypeId = "601"
Taxes1.Amount = "220000"
Taxes1.Rate = "2200"
Taxes1.BaseAmount = "1000000"

Taxes.add(Taxes1);

pspAmountAdditionalDetails.Taxes = Taxes

PayOnLine3p.psp_AmountAdditionalDetails = pspAmountAdditionalDetails

pspBillingDetails := nps.NewBillingDetailsStruct()
pspBillingDetails.Invoice = "A00024144"
pspBillingDetails.InvoiceAmount = "1600000"
pspBillingDetails.InvoiceCurrency = "858"

PayOnLine3p.psp_BillingDetails = pspBillingDetails

response, err := service.PayOnLine_3p(PayOnLine3p)

if err != nil {
    fmt.Printf("Error: = [%s]", err)
}
fmt.Printf("Response = [%s] [%s]", resp.Psp_ResponseCod, resp.Psp_ResponseMsg)
fmt.Printf("Extended = [%s]", resp.Psp_ResponseExtended)



