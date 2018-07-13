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

pspTransactions := nps.NewTransactionsStruct()

pspTransactions1 := pspTransactions.Items[1];
pspTransactions1.Psp_MerchantId = "sdk_test"
pspTransactions1.Psp_MerchTxRef = "ORDER66666-3"
pspTransactions1.Psp_Product = "14"
pspTransactions1.Psp_Amount = "1360000"
pspTransactions1.Psp_NumPayments = "1"

pspAmountAdditionalDetails := nps.NewAmountAdditionalDetailsStruct()
pspAmountAdditionalDetails.Tip = "20"
pspAmountAdditionalDetails.Discount = "1"

Taxes := nps.NewTaxesStruct()

Taxes1 := Taxes.Items[1];
Taxes1.TypeId = "100"
Taxes1.Amount = "200000"

Taxes2 := Taxes.Items[2];
Taxes2.TypeId = "501"
Taxes2.Amount = "160000"
Taxes2.Rate = "1600"
Taxes2.BaseAmount = "1000000"


pspAmountAdditionalDetails.Taxes = Taxes

pspTransactions1.psp_AmountAdditionalDetails = pspAmountAdditionalDetails

pspTransactions2 := pspTransactions.Items[2];
pspTransactions2.Psp_MerchantId = "sdk_test"
pspTransactions2.Psp_MerchTxRef = "ORDER66666-3"
pspTransactions2.Psp_Product = "14"
pspTransactions2.Psp_Amount = "1360000"
pspTransactions2.Psp_NumPayments = "1"

pspAmountAdditionalDetails := nps.NewAmountAdditionalDetailsStruct()
pspAmountAdditionalDetails.Tip = "20"
pspAmountAdditionalDetails.Discount = "1"

Taxes := nps.NewTaxesStruct()

Taxes1 := Taxes.Items[1];
Taxes1.TypeId = "100"
Taxes1.Amount = "200000"

Taxes2 := Taxes.Items[2];
Taxes2.TypeId = "501"
Taxes2.Amount = "160000"
Taxes2.Rate = "1600"
Taxes2.BaseAmount = "1000000"


pspAmountAdditionalDetails.Taxes = Taxes

pspTransactions2.psp_AmountAdditionalDetails = pspAmountAdditionalDetails


SplitPayOnLine3p.psp_Transactions = pspTransactions

response, err := service.SplitPayOnLine_3p(SplitPayOnLine3p)

if err != nil {
    fmt.Printf("Error: = [%s]", err)
}
fmt.Printf("Response = [%s] [%s]", resp.Psp_ResponseCod, resp.Psp_ResponseMsg)
fmt.Printf("Extended = [%s]", resp.Psp_ResponseExtended)



