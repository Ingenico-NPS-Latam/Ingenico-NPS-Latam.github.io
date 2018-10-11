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
SplitPayOnLine3p.Psp_MerchantId = "sdk_test"
SplitPayOnLine3p.Psp_TxSource = "WEB"
SplitPayOnLine3p.Psp_MerchOrderId = "ORDER66666"
SplitPayOnLine3p.Psp_ReturnURL = "http://localhost/"
SplitPayOnLine3p.Psp_FrmLanguage = "es_AR"
SplitPayOnLine3p.Psp_Amount = "2720000"
SplitPayOnLine3p.Psp_Currency = "170"
SplitPayOnLine3p.Psp_Country = "COL"
SplitPayOnLine3p.Psp_Product = "14"
SplitPayOnLine3p.Psp_PosDateTime = "2019-12-01 12:00:00"

pspTransactions := nps.NewArrayOf_TransactionsStruct()
pspTransactions.Items = make([]*nps.NewTransactionsStruct(), 0)

pspTransactions1 := nps.NewpspTransactionsStruct()
pspTransactions1.Psp_MerchantId = "sdk_test"
pspTransactions1.Psp_MerchTxRef = "ORDER66666-3"
pspTransactions1.Psp_Product = "14"
pspTransactions1.Psp_Amount = "1360000"
pspTransactions1.Psp_NumPayments = "1"

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

pspTransactions1.psp_AmountAdditionalDetails = pspAmountAdditionalDetails

pspTransactions.Items = append(pspTransactions.Items, pspTransactions1)
pspTransactions2 := nps.NewpspTransactionsStruct()
pspTransactions2.Psp_MerchantId = "sdk_test"
pspTransactions2.Psp_MerchTxRef = "ORDER66666-3"
pspTransactions2.Psp_Product = "14"
pspTransactions2.Psp_Amount = "1360000"
pspTransactions2.Psp_NumPayments = "1"

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

pspTransactions2.psp_AmountAdditionalDetails = pspAmountAdditionalDetails

pspTransactions.Items = append(pspTransactions.Items, pspTransactions2)

response, err := service.SplitPayOnLine_3p(SplitPayOnLine3p)

if err != nil {
    fmt.Printf("Error: = [%s]", err)
}
fmt.Printf("Response = [%s] [%s]", resp.Psp_ResponseCod, resp.Psp_ResponseMsg)
fmt.Printf("Extended = [%s]", resp.Psp_ResponseExtended)



