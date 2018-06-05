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
Authorize2p.Psp_MerchantId = "sdk_test"
Authorize2p.Psp_TxSource = "WEB"
Authorize2p.Psp_MerchTxRef = "ORDERX1466Xz-3"
Authorize2p.Psp_MerchOrderId = "ORDERX1466Xz"
Authorize2p.Psp_Amount = "1220000"
Authorize2p.Psp_NumPayments = "1"
Authorize2p.Psp_Currency = "858"
Authorize2p.Psp_Country = "URY"
Authorize2p.Psp_Product = "5"
Authorize2p.Psp_CardNumber = "5453010000083303"
Authorize2p.Psp_CardExpDate = "1904"
Authorize2p.Psp_PosDateTime = "2019-12-01 12:00:00"

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

Authorize2p.psp_AmountAdditionalDetails = pspAmountAdditionalDetails

pspBillingDetails := nps.NewBillingDetailsStruct()
pspBillingDetails.Invoice = "A00024144"
pspBillingDetails.InvoiceAmount = "1600000"
pspBillingDetails.InvoiceCurrency = "858"

Authorize2p.psp_BillingDetails = pspBillingDetails

response, err := service.Authorize_2p(Authorize2p)

if err != nil {
    fmt.Printf("Error: = [%s]", err)
}
fmt.Printf("Response = [%s] [%s]", resp.Psp_ResponseCod, resp.Psp_ResponseMsg)
fmt.Printf("Extended = [%s]", resp.Psp_ResponseExtended)



