local nps = require("npssdk")
nps.configuration.environment= nps.SANDBOX_ENV
nps.configuration.secret_key = "_YOUR_SECRET_KEY_"


payonline3p = {}

payonline3p.psp_Version = "2.2"
payonline3p.psp_MerchantId = "sdk_test"
payonline3p.psp_TxSource = "WEB"
payonline3p.psp_MerchTxRef = "ORDER76666-3"
payonline3p.psp_MerchOrderId = "ORDER76666"
payonline3p.psp_ReturnURL = "http://localhost/"
payonline3p.psp_FrmLanguage = "es_AR"
payonline3p.psp_Amount = "1360000"
payonline3p.psp_NumPayments = "1"
payonline3p.psp_Currency = "170"
payonline3p.psp_Country = "COL"
payonline3p.psp_Product = "14"
payonline3p.psp_PosDateTime = "2019-12-01 12:00:00"

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

payonline3p.psp_AmountAdditionalDetails = pspAmountAdditionalDetails

response = nps.pay_online_3p(payonline3p)

print(resp.psp_ResponseCod)
