package main

import (
        "fmt"
        "log"
        "npsSdk"
        CONSTANTS "npsSdk/constants"
)

service:= nps.NewPaymentServicePlatformPortType(true)

SplitPayOnLine3p := nps.NewRequerimientoStruct_SplitPayOnLine_3p()

SplitPayOnLine3p.Psp_Version = "2.2"
SplitPayOnLine3p.Psp_MerchantId = "psp_test"
SplitPayOnLine3p.Psp_TxSource = "WEB"
SplitPayOnLine3p.Psp_MerchOrderId = "ORDER66666"
SplitPayOnLine3p.Psp_ReturnURL = "http://localhost/"
SplitPayOnLine3p.Psp_FrmLanguage = "es_AR"
SplitPayOnLine3p.Psp_Amount = "62400"
SplitPayOnLine3p.Psp_Currency = "840"
SplitPayOnLine3p.Psp_Country = "ECU"
SplitPayOnLine3p.Psp_Product = "14"
SplitPayOnLine3p.Psp_PosDateTime = "2019-12-01 12:00:00"

pspTransactions := nps.NewTransactionsStruct()

pspTransactions1 := pspTransactions.Items[1];
pspTransactions1.Psp_MerchantId = "psp_test"
pspTransactions1.Psp_MerchTxRef = "ORDER66666-3"
pspTransactions1.Psp_Product = "14"
pspTransactions1.Psp_Amount = "31200"
pspTransactions1.Psp_NumPayments = "1"

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

pspTransactions1.psp_AmountAdditionalDetails = pspAmountAdditionalDetails

pspTransactions2 := pspTransactions.Items[2];
pspTransactions2.Psp_MerchantId = "psp_test"
pspTransactions2.Psp_MerchTxRef = "ORDER66666-3"
pspTransactions2.Psp_Product = "14"
pspTransactions2.Psp_Amount = "31200"
pspTransactions2.Psp_NumPayments = "1"

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

pspTransactions2.psp_AmountAdditionalDetails = pspAmountAdditionalDetails


SplitPayOnLine3p.psp_Transactions = pspTransactions

response, err := service.SplitPayOnLine_3p(SplitPayOnLine3p)

if err != nil {
    fmt.Printf("Error: = [%s]", err)
}
fmt.Printf("Response = [%s] [%s]", resp.Psp_ResponseCod, resp.Psp_ResponseMsg)
fmt.Printf("Extended = [%s]", resp.Psp_ResponseExtended)



