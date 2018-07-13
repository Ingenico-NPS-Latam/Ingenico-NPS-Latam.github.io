ArraySplitAuthorize3pTransactions := nps.NewArraySplitAuthorize3pTransactionsStruct()
ArraySplitAuthorize3pTransactions.Psp_MerchantId = "sdk_test"
ArraySplitAuthorize3pTransactions.Psp_MerchTxRef = "ORDER1000-1"
ArraySplitAuthorize3pTransactions.Psp_MerchAdditionalRef = "ADDITIONAL-REF1234"
ArraySplitAuthorize3pTransactions.Psp_Product = "14"
ArraySplitAuthorize3pTransactions.Psp_PromotionCore = "VISA SANTANDER"
ArraySplitAuthorize3pTransactions.Psp_Amount = "15050"
ArraySplitAuthorize3pTransactions.Psp_NumPayments = "1"
ArraySplitAuthorize3pTransactions.Psp_SoftDescriptor = "Compra Art 15"

pspAmountAdditionalDetails := nps.NewAmountAdditionalDetailsRequestStruct()
pspAmountAdditionalDetails.Tip = "20000"
pspAmountAdditionalDetails.Discount = "11000"

Taxes := nps.NewArrayOf_TaxesRequestStruct()
Taxes.Items = make([]*nps.NewTaxesRequestStruct(), 0)

Taxes1 := nps.NewTaxesRequestStruct()
Taxes1.TypeId = "500"
Taxes1.Amount = "10000"
Taxes1.Rate = "2100"
Taxes1.BaseAmount = "10000"
Taxes.Items = append(Taxes.Items, Taxes1)

Taxes2 := nps.NewTaxesRequestStruct()
Taxes2.TypeId = "500"
Taxes2.Amount = "10000"
Taxes2.Rate = "2100"
Taxes2.BaseAmount = "10000"
Taxes.Items = append(Taxes.Items, Taxes2)


ArraySplitAuthorize3pTransactions.psp_AmountAdditionalDetails = pspAmountAdditionalDetails
