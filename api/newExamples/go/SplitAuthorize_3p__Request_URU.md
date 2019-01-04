package main

import (
    "fmt"
    "github.com/Ingenico-NPS-Latam/nps-sdk-go/npsSdk"
    CONSTANTS "github.com/Ingenico-NPS-Latam/nps-sdk-go/npsSdk/constants"
)

func main() {

err := npsSdk.Configure(map[string]interface{}(
    "environment": CONSTANTS.SANDBOX_ENV,
    "secret_key": "_YOUR_SECRET_KEY_",
    "debug": true,
    "log_level": CONSTANTS.DEBUG,
})

service := npsSdk.NewPaymentServicePlatformPortType(true)

SplitAuthorize3p := npsSdk.NewRequerimientoStruct_SplitAuthorize_3p()

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

pspTransactions := nps.NewArrayOf_TransactionsStruct()
pspTransactions.Items = make([]*nps.NewTransactionsStruct(), 0)

pspTransactions1 := nps.NewpspTransactionsStruct()
pspTransactions1.Psp_MerchantId = "sdk_test"
pspTransactions1.Psp_MerchTxRef = "ORDER66666-3"
pspTransactions1.Psp_Product = "5"
pspTransactions1.Psp_Amount = "1220000"
pspTransactions1.Psp_NumPayments = "1"

pspAmountAdditionalDetails := nps.NewAmountAdditionalDetailsRequestStruct()
pspAmountAdditionalDetails.Tip = "20"
pspAmountAdditionalDetails.Discount = "1"

Taxes := nps.NewArrayOf_TaxesRequestStruct()
Taxes.Items = make([]*nps.NewTaxesRequestStruct(), 0)

Taxes1 := nps.NewTaxesRequestStruct()
Taxes1.TypeId = "601"
Taxes1.Amount = "220000"
Taxes1.Rate = "2200"
Taxes1.BaseAmount = "1000000"
Taxes.Items = append(Taxes.Items, Taxes1)


pspTransactions1.psp_AmountAdditionalDetails = pspAmountAdditionalDetails
pspTransactions.Items = append(pspTransactions.Items, pspTransactions1)

pspTransactions2 := nps.NewpspTransactionsStruct()
pspTransactions2.Psp_MerchantId = "sdk_test"
pspTransactions2.Psp_MerchTxRef = "ORDER66666-3"
pspTransactions2.Psp_Product = "5"
pspTransactions2.Psp_Amount = "1220000"
pspTransactions2.Psp_NumPayments = "1"

pspAmountAdditionalDetails := nps.NewAmountAdditionalDetailsRequestStruct()
pspAmountAdditionalDetails.Tip = "20"
pspAmountAdditionalDetails.Discount = "1"

Taxes := nps.NewArrayOf_TaxesRequestStruct()
Taxes.Items = make([]*nps.NewTaxesRequestStruct(), 0)

Taxes1 := nps.NewTaxesRequestStruct()
Taxes1.TypeId = "601"
Taxes1.Amount = "220000"
Taxes1.Rate = "2200"
Taxes1.BaseAmount = "1000000"
Taxes.Items = append(Taxes.Items, Taxes1)


pspTransactions2.psp_AmountAdditionalDetails = pspAmountAdditionalDetails
pspTransactions.Items = append(pspTransactions.Items, pspTransactions2)


resp, err := service.SplitAuthorize_3p(SplitAuthorize3p)

if err != nil {
    fmt.Printf("Error: = [%s]", err)
}
fmt.Printf("Response = [%s] [%s]", resp.Psp_ResponseCod, resp.Psp_ResponseMsg)
fmt.Printf("Extended = [%s]", resp.Psp_ResponseExtended)
