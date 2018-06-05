local nps = require("npssdk")
nps.configuration.environment= nps.SANDBOX_ENV
nps.configuration.secret_key = "_YOUR_SECRET_KEY_"


payonline2p = {}

payonline2p.psp_Version = "2.2"
payonline2p.psp_MerchantId = "sdk_test"
payonline2p.psp_TxSource = "WEB"
payonline2p.psp_MerchTxRef = "ORDER69461-3"
payonline2p.psp_MerchOrderId = "ORDER69461"
payonline2p.psp_Amount = "15050"
payonline2p.psp_NumPayments = "1"
payonline2p.psp_Currency = "032"
payonline2p.psp_Country = "ARG"
payonline2p.psp_Product = "14"
payonline2p.psp_CardNumber = "4507990000000010"
payonline2p.psp_CardExpDate = "1912"
payonline2p.psp_CardSecurityCode = "325"
payonline2p.psp_PosDateTime = "2019-12-01 12:00:00"

response = nps.pay_online_2p(payonline2p)

print(resp.psp_ResponseCod)
