local nps = require("npssdk")
nps.configuration.environment= nps.SANDBOX_ENV
nps.configuration.secret_key = "_YOUR_SECRET_KEY_"


splitpayonline3p = {}

splitpayonline3p.psp_Version = "2.2"
splitpayonline3p.psp_MerchantId = "sdk_test"
splitpayonline3p.psp_TxSource = "WEB"
splitpayonline3p.psp_MerchOrderId = "ORDER66666"
splitpayonline3p.psp_ReturnURL = "http://localhost/"
splitpayonline3p.psp_FrmLanguage = "es_AR"
splitpayonline3p.psp_Amount = "2720000"
splitpayonline3p.psp_Currency = "170"
splitpayonline3p.psp_Country = "COL"
splitpayonline3p.psp_Product = "14"
splitpayonline3p.psp_PosDateTime = "2019-12-01 12:00:00"

pspTransactions = {}

pspTransactions1 = {}
pspTransactions1.psp_MerchantId = "sdk_test"
pspTransactions1.psp_MerchTxRef = "ORDER66666-3"
pspTransactions1.psp_Product = "14"
pspTransactions1.psp_Amount = "1360000"
pspTransactions1.psp_NumPayments = "1"

pspAmountAdditionalDetails = {}
pspAmountAdditionalDetails.Tip = "20"
pspAmountAdditionalDetails.Discount = "1"

Taxes = {}

Taxes1 = {}
Taxes1.TypeId = "100"
Taxes1.Amount = "200000"

Taxes[#Taxes+1] = Taxes1

Taxes2 = {}
Taxes2.TypeId = "501"
Taxes2.Amount = "160000"
Taxes2.Rate = "1600"
Taxes2.BaseAmount = "1000000"

Taxes[#Taxes+1] = Taxes2

pspAmountAdditionalDetails.Taxes = Taxes

pspTransactions1.psp_AmountAdditionalDetails = pspAmountAdditionalDetails

pspTransactions[#pspTransactions+1] = pspTransactions1

pspTransactions2 = {}
pspTransactions2.psp_MerchantId = "sdk_test"
pspTransactions2.psp_MerchTxRef = "ORDER66666-3"
pspTransactions2.psp_Product = "14"
pspTransactions2.psp_Amount = "1360000"
pspTransactions2.psp_NumPayments = "1"

pspAmountAdditionalDetails = {}
pspAmountAdditionalDetails.Tip = "20"
pspAmountAdditionalDetails.Discount = "1"

Taxes = {}

Taxes1 = {}
Taxes1.TypeId = "100"
Taxes1.Amount = "200000"

Taxes[#Taxes+1] = Taxes1

Taxes2 = {}
Taxes2.TypeId = "501"
Taxes2.Amount = "160000"
Taxes2.Rate = "1600"
Taxes2.BaseAmount = "1000000"

Taxes[#Taxes+1] = Taxes2

pspAmountAdditionalDetails.Taxes = Taxes

pspTransactions2.psp_AmountAdditionalDetails = pspAmountAdditionalDetails

pspTransactions[#pspTransactions+1] = pspTransactions2

splitpayonline3p.psp_Transactions = pspTransactions

response = nps.split_pay_online_3p(splitpayonline3p)

print(resp.psp_ResponseCod)
