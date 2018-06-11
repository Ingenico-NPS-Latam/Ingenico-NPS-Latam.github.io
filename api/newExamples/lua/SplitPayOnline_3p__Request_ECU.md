local nps = require("npssdk")
nps.configuration.environment= nps.SANDBOX_ENV
nps.configuration.secret_key = "_YOUR_SECRET_KEY_"


splitpayonline3p = {}

splitpayonline3p.psp_Version = "2.2"
splitpayonline3p.psp_MerchantId = "psp_test"
splitpayonline3p.psp_TxSource = "WEB"
splitpayonline3p.psp_MerchOrderId = "ORDER66666"
splitpayonline3p.psp_ReturnURL = "http://localhost/"
splitpayonline3p.psp_FrmLanguage = "es_AR"
splitpayonline3p.psp_Amount = "62400"
splitpayonline3p.psp_Currency = "840"
splitpayonline3p.psp_Country = "ECU"
splitpayonline3p.psp_Product = "14"
splitpayonline3p.psp_PosDateTime = "2019-12-01 12:00:00"

pspTransactions = {}

pspTransactions1 = {}
pspTransactions1.psp_MerchantId = "psp_test"
pspTransactions1.psp_MerchTxRef = "ORDER66666-3"
pspTransactions1.psp_Product = "14"
pspTransactions1.psp_Amount = "31200"
pspTransactions1.psp_NumPayments = "1"

pspAmountAdditionalDetails = {}

Taxes = {}

Taxes1 = {}
Taxes1.TypeId = "700"
Taxes1.Amount = "1200"
Taxes1.Rate = "1200"
Taxes1.BaseAmount = "100000"

Taxes[#Taxes+1] = Taxes1

Taxes2 = {}
Taxes2.TypeId = "701"
Taxes2.BaseAmount = "20000"

Taxes[#Taxes+1] = Taxes2

pspAmountAdditionalDetails.Taxes = Taxes

pspTransactions1.psp_AmountAdditionalDetails = pspAmountAdditionalDetails

pspTransactions[#pspTransactions+1] = pspTransactions1

pspTransactions2 = {}
pspTransactions2.psp_MerchantId = "psp_test"
pspTransactions2.psp_MerchTxRef = "ORDER66666-3"
pspTransactions2.psp_Product = "14"
pspTransactions2.psp_Amount = "31200"
pspTransactions2.psp_NumPayments = "1"

pspAmountAdditionalDetails = {}

Taxes = {}

Taxes1 = {}
Taxes1.TypeId = "700"
Taxes1.Amount = "1200"
Taxes1.Rate = "1200"
Taxes1.BaseAmount = "100000"

Taxes[#Taxes+1] = Taxes1

Taxes2 = {}
Taxes2.TypeId = "701"
Taxes2.BaseAmount = "20000"

Taxes[#Taxes+1] = Taxes2

pspAmountAdditionalDetails.Taxes = Taxes

pspTransactions2.psp_AmountAdditionalDetails = pspAmountAdditionalDetails

pspTransactions[#pspTransactions+1] = pspTransactions2

splitpayonline3p.psp_Transactions = pspTransactions

response = nps.split_pay_online_3p(splitpayonline3p)

print(resp.psp_ResponseCod)
