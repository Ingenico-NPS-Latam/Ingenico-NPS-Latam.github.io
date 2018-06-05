local nps = require("npssdk")
nps.configuration.environment= nps.SANDBOX_ENV
nps.configuration.secret_key = "_YOUR_SECRET_KEY_"


fraudscreening = {}

fraudscreening.psp_Version = "2.2"
fraudscreening.psp_MerchantId = "sdk_test"
fraudscreening.psp_TxSource = "WEB"
fraudscreening.psp_MerchTxRef = "ORDER66666-3"
fraudscreening.psp_MerchOrderId = "ORDER66666"
fraudscreening.psp_Amount = "15050"
fraudscreening.psp_NumPayments = "1"
fraudscreening.psp_Currency = "032"
fraudscreening.psp_Country = "ARG"
fraudscreening.psp_Product = "14"
fraudscreening.psp_CardNumber = "4507990000000010"
fraudscreening.psp_CardExpDate = "1912"
fraudscreening.psp_PosDateTime = "2019-12-01 12:00:00"

response = nps.fraud_screening(fraudscreening)

print(resp.psp_ResponseCod)
