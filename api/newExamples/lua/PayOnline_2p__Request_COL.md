local nps = require("npssdk")
nps.configuration.environment= nps.SANDBOX_ENV
nps.configuration.secret_key = "_YOUR_SECRET_KEY_"


payonline2p = {}

payonline2p.psp_Version = "2.2"
payonline2p.psp_MerchantId = "sdk_test"
payonline2p.psp_TxSource = "WEB"
payonline2p.psp_MerchTxRef = "ORDERX1466Xz-3"
payonline2p.psp_MerchOrderId = "ORDERX1466Xz"
payonline2p.psp_Amount = "1360000"
payonline2p.psp_NumPayments = "1"
payonline2p.psp_Currency = "170"
payonline2p.psp_Country = "COL"
payonline2p.psp_Product = "14"
payonline2p.psp_CardNumber = "4005580000050003"
payonline2p.psp_CardExpDate = "1812"
payonline2p.psp_PosDateTime = "2019-12-01 12:00:00"

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

payonline2p.psp_AmountAdditionalDetails = pspAmountAdditionalDetails

response = nps.pay_online_2p(payonline2p)

print(resp.psp_ResponseCod)
