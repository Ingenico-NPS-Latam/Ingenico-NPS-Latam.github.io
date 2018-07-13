ArraySplitPayOnline3pTransactions = {}

ArraySplitPayOnline3pTransactions.psp_MerchantId = "sdk_test"
ArraySplitPayOnline3pTransactions.psp_MerchTxRef = "ORDER1000-1"
ArraySplitPayOnline3pTransactions.psp_MerchAdditionalRef = "ADDITIONAL-REF1234"
ArraySplitPayOnline3pTransactions.psp_Product = "14"
ArraySplitPayOnline3pTransactions.psp_PromotionCode = "VISA SANTANDER"
ArraySplitPayOnline3pTransactions.psp_Amount = "15050"
ArraySplitPayOnline3pTransactions.psp_NumPayments = "1"
ArraySplitPayOnline3pTransactions.psp_SoftDescriptor = "Compra Art 15"

pspAmountAdditionalDetails = {}
pspAmountAdditionalDetails.Tip = "20000"
pspAmountAdditionalDetails.Discount = "11000"

Taxes = {}

Taxes1 = {}
Taxes1.TypeId = "500"
Taxes1.Amount = "10000"
Taxes1.Rate = "2100"
Taxes1.BaseAmount = "10000"

Taxes[#Taxes+1] = Taxes1

Taxes2 = {}
Taxes2.TypeId = "500"
Taxes2.Amount = "10000"
Taxes2.Rate = "2100"
Taxes2.BaseAmount = "10000"

Taxes[#Taxes+1] = Taxes2

pspAmountAdditionalDetails.Taxes = Taxes

ArraySplitPayOnline3pTransactions.psp_AmountAdditionalDetails = pspAmountAdditionalDetails
