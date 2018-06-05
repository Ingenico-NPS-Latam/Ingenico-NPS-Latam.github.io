package main

import (
        "fmt"
        "log"
        "npsSdk"
        CONSTANTS "npsSdk/constants"
)

service:= nps.NewPaymentServicePlatformPortType(true)

SplitAuthorize3p := nps.NewRequerimientoStruct_SplitAuthorize_3p()

SplitAuthorize3p.Psp_Version = "2.2"
SplitAuthorize3p.Psp_MerchantId = "sdk_test"
SplitAuthorize3p.Psp_TxSource = "WEB"
SplitAuthorize3p.Psp_MerchOrderId = "ORDER66666"
SplitAuthorize3p.Psp_ReturnURL = "http://localhost/"
SplitAuthorize3p.Psp_FrmLanguage = "es_AR"
SplitAuthorize3p.Psp_Amount = "2440000"
SplitAuthorize3p.Psp_Currency = "858"
SplitAuthorize3p.Psp_Country = "URY"
SplitAuthorize3p.Psp_Product = "5"
SplitAuthorize3p.Psp_PosDateTime = "2019-12-01 12:00:00"

pspBillingDetails := nps.NewBillingDetailsStruct()
pspBillingDetails.Invoice = "A00024144"
pspBillingDetails.InvoiceAmount = "1600000"
pspBillingDetails.InvoiceCurrency = "858"

SplitAuthorize3p.psp_BillingDetails = pspBillingDetails

ComplexElementArray pspTransactions = new ComplexElementArray();

ComplexElementArrayItem pspTransactions1 = new ComplexElementArrayItem();
pspTransactions1.Psp_MerchantId = "sdk_test"
pspTransactions1.Psp_MerchTxRef = "ORDER66666-3"
pspTransactions1.Psp_Product = "5"
pspTransactions1.Psp_Amount = "1220000"
pspTransactions1.Psp_NumPayments = "1"

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

pspTransactions1.psp_AmountAdditionalDetails = pspAmountAdditionalDetails

pspTransactions.add(pspTransactions1);

ComplexElementArrayItem pspTransactions2 = new ComplexElementArrayItem();
pspTransactions2.Psp_MerchantId = "sdk_test"
pspTransactions2.Psp_MerchTxRef = "ORDER66666-3"
pspTransactions2.Psp_Product = "5"
pspTransactions2.Psp_Amount = "1220000"
pspTransactions2.Psp_NumPayments = "1"

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

pspTransactions2.psp_AmountAdditionalDetails = pspAmountAdditionalDetails

pspTransactions.add(pspTransactions2);

SplitAuthorize3p.psp_Transactions = pspTransactions

response, err := service.SplitAuthorize_3p(SplitAuthorize3p)

if err != nil {
    fmt.Printf("Error: = [%s]", err)
}
fmt.Printf("Response = [%s] [%s]", resp.Psp_ResponseCod, resp.Psp_ResponseMsg)
fmt.Printf("Extended = [%s]", resp.Psp_ResponseExtended)



