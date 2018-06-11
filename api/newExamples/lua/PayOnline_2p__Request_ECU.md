local nps = require("npssdk")
nps.configuration.environment= nps.SANDBOX_ENV
nps.configuration.secret_key = "_YOUR_SECRET_KEY_"


payonline2p = {}

payonline2p.psp_Version = "2.2"
payonline2p.psp_MerchantId = "psp_test"
payonline2p.psp_TxSource = "WEB"
payonline2p.psp_MerchTxRef = "ORDERX1466Xz-3"
payonline2p.psp_MerchOrderId = "ORDERX1466Xz"
payonline2p.psp_NumPayments = "1"
payonline2p.psp_Currency = "840"
payonline2p.psp_Country = "ECU"
payonline2p.psp_Product = "5"
payonline2p.psp_CardNumber = "5189680000495961"
payonline2p.psp_CardExpDate = "3311"
payonline2p.psp_PosDateTime = "2019-12-01 12:00:00"
payonline2p.psp_Amount = "31200"

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

payonline2p.psp_AmountAdditionalDetails = pspAmountAdditionalDetails

response = nps.pay_online_2p(payonline2p)

print(resp.psp_ResponseCod)
