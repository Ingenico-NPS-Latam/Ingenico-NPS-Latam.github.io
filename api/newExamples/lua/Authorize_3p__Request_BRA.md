local nps = require("npssdk")
nps.configuration.environment= nps.SANDBOX_ENV
nps.configuration.secret_key = "_YOUR_SECRET_KEY_"


authorize3p = {}

authorize3p.psp_Version = "2.2"
authorize3p.psp_MerchantId = "sdk_test"
authorize3p.psp_TxSource = "WEB"
authorize3p.psp_MerchTxRef = "ORDER76666-3"
authorize3p.psp_MerchOrderId = "ORDER76666"
authorize3p.psp_ReturnURL = "http://localhost/"
authorize3p.psp_FrmLanguage = "es_AR"
authorize3p.psp_Amount = "1200000"
authorize3p.psp_NumPayments = "1"
authorize3p.psp_Currency = "986"
authorize3p.psp_Country = "BRA"
authorize3p.psp_Product = "14"
authorize3p.psp_PosDateTime = "2019-12-01 12:00:00"

pspAmountAdditionalDetails = {}
pspAmountAdditionalDetails.Tip = "20"
pspAmountAdditionalDetails.Discount = "1"

Taxes = {}

Taxes1 = {}
Taxes1.TypeId = "100"
Taxes1.Amount = "200000"

Taxes[#Taxes+1] = Taxes1

pspAmountAdditionalDetails.Taxes = Taxes

authorize3p.psp_AmountAdditionalDetails = pspAmountAdditionalDetails

response = nps.authorize_3p(authorize3p)

print(resp.psp_ResponseCod)
