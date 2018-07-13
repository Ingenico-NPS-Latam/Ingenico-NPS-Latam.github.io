ArraySplitAuthorize3pTransactions = {}

ArraySplitAuthorize3pTransactions.psp_MerchantId = "sdk_test"
ArraySplitAuthorize3pTransactions.psp_MerchTxRef = "ORDER1000-1"
ArraySplitAuthorize3pTransactions.psp_MerchAdditionalRef = "ADDITIONAL-REF1234"
ArraySplitAuthorize3pTransactions.psp_Product = "14"
ArraySplitAuthorize3pTransactions.psp_PromotionCore = "VISA SANTANDER"
ArraySplitAuthorize3pTransactions.psp_Amount = "15050"
ArraySplitAuthorize3pTransactions.psp_NumPayments = "1"
ArraySplitAuthorize3pTransactions.psp_SoftDescriptor = "Compra Art 15"

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

ArraySplitAuthorize3pTransactions.psp_AmountAdditionalDetails = pspAmountAdditionalDetails
