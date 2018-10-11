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
SplitAuthorize3p.Psp_Amount = "2400000"
SplitAuthorize3p.Psp_Currency = "986"
SplitAuthorize3p.Psp_Country = "BRA"
SplitAuthorize3p.Psp_Product = "14"
SplitAuthorize3p.Psp_PosDateTime = "2019-12-01 12:00:00"

pspTransactions := nps.NewArrayOf_TransactionsStruct()
pspTransactions.Items = make([]*nps.NewTransactionsStruct(), 0)

pspTransactions1 := nps.NewpspTransactionsStruct()
pspTransactions1.Psp_MerchantId = "sdk_test"
pspTransactions1.Psp_MerchTxRef = "ORDER66666-3"
pspTransactions1.Psp_Product = "14"
pspTransactions1.Psp_Amount = "1200000"
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

pspTransactions1.psp_AmountAdditionalDetails = pspAmountAdditionalDetails

pspTransactions.Items = append(pspTransactions.Items, pspTransactions1)
pspTransactions2 := nps.NewpspTransactionsStruct()
pspTransactions2.Psp_MerchantId = "sdk_test"
pspTransactions2.Psp_MerchTxRef = "ORDER66666-3"
pspTransactions2.Psp_Product = "14"
pspTransactions2.Psp_Amount = "1200000"
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

pspTransactions2.psp_AmountAdditionalDetails = pspAmountAdditionalDetails

pspTransactions.Items = append(pspTransactions.Items, pspTransactions2)

response, err := service.SplitAuthorize_3p(SplitAuthorize3p)

if err != nil {
    fmt.Printf("Error: = [%s]", err)
}
fmt.Printf("Response = [%s] [%s]", resp.Psp_ResponseCod, resp.Psp_ResponseMsg)
fmt.Printf("Extended = [%s]", resp.Psp_ResponseExtended)



