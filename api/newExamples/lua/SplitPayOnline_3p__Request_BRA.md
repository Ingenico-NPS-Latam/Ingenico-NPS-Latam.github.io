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
splitpayonline3p.psp_Amount = "2400000"
splitpayonline3p.psp_Currency = "986"
splitpayonline3p.psp_Country = "BRA"
splitpayonline3p.psp_Product = "14"
splitpayonline3p.psp_PosDateTime = "2019-12-01 12:00:00"

pspTransactions = {}

pspTransactions1 = {}
pspTransactions1.psp_MerchantId = "sdk_test"
pspTransactions1.psp_MerchTxRef = "ORDER66666-3"
pspTransactions1.psp_Product = "14"
pspTransactions1.psp_Amount = "1200000"
pspTransactions1.psp_NumPayments = "1"

pspAmountAdditionalDetails = {}
pspAmountAdditionalDetails.Tip = "20"
pspAmountAdditionalDetails.Discount = "1"

Taxes = {}

Taxes1 = {}
Taxes1.TypeId = "100"
Taxes1.Amount = "200000"

Taxes[#Taxes+1] = Taxes1

pspAmountAdditionalDetails.Taxes = Taxes

pspTransactions1.psp_AmountAdditionalDetails = pspAmountAdditionalDetails

pspTransactions[#pspTransactions+1] = pspTransactions1

pspTransactions2 = {}
pspTransactions2.psp_MerchantId = "sdk_test"
pspTransactions2.psp_MerchTxRef = "ORDER66666-3"
pspTransactions2.psp_Product = "14"
pspTransactions2.psp_Amount = "1200000"
pspTransactions2.psp_NumPayments = "1"

pspAmountAdditionalDetails = {}
pspAmountAdditionalDetails.Tip = "20"
pspAmountAdditionalDetails.Discount = "1"

Taxes = {}

Taxes1 = {}
Taxes1.TypeId = "100"
Taxes1.Amount = "200000"

Taxes[#Taxes+1] = Taxes1

pspAmountAdditionalDetails.Taxes = Taxes

pspTransactions2.psp_AmountAdditionalDetails = pspAmountAdditionalDetails

pspTransactions[#pspTransactions+1] = pspTransactions2

splitpayonline3p.psp_Transactions = pspTransactions

response = nps.split_pay_online_3p(splitpayonline3p)

print(resp.psp_ResponseCod)
