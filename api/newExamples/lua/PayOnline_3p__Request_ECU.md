local nps = require("npssdk")
nps.configuration.environment= nps.SANDBOX_ENV
nps.configuration.secret_key = "_YOUR_SECRET_KEY_"


payonline3p = {}

payonline3p.psp_Version = "2.2"
payonline3p.psp_MerchantId = "psp_test"
payonline3p.psp_TxSource = "WEB"
payonline3p.psp_MerchTxRef = "ORDER76666-3"
payonline3p.psp_MerchOrderId = "ORDER76666"
payonline3p.psp_ReturnURL = "http://localhost/"
payonline3p.psp_FrmLanguage = "es_AR"
payonline3p.psp_NumPayments = "1"
payonline3p.psp_Currency = "840"
payonline3p.psp_Country = "ECU"
payonline3p.psp_Product = "14"
payonline3p.psp_PosDateTime = "2019-12-01 12:00:00"
payonline3p.psp_Amount = "31200"

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

payonline3p.psp_AmountAdditionalDetails = pspAmountAdditionalDetails

response = nps.pay_online_3p(payonline3p)

print(resp.psp_ResponseCod)
