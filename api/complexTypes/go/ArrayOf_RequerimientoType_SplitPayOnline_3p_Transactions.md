ArraySplitPayOnline3pTransactions := nps.NewArraySplitPayOnline3pTransactionsStruct()
ArraySplitPayOnline3pTransactions.Psp_MerchantId = "sdk_test"
ArraySplitPayOnline3pTransactions.Psp_MerchTxRef = "ORDER1000-1"
ArraySplitPayOnline3pTransactions.Psp_MerchAdditionalRef = "ADDITIONAL-REF1234"
ArraySplitPayOnline3pTransactions.Psp_Product = "14"
ArraySplitPayOnline3pTransactions.Psp_PromotionCode = "VISA SANTANDER"
ArraySplitPayOnline3pTransactions.Psp_Amount = "15050"
ArraySplitPayOnline3pTransactions.Psp_NumPayments = "1"
ArraySplitPayOnline3pTransactions.Psp_SoftDescriptor = "Compra Art 15"

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


ArraySplitPayOnline3pTransactions.psp_AmountAdditionalDetails = pspAmountAdditionalDetails
