local nps = require("npssdk")
nps.configuration.environment= nps.SANDBOX_ENV
nps.configuration.secret_key = "_YOUR_SECRET_KEY_"


capture = {}

capture.psp_Version = "2.2"
capture.psp_MerchantId = "sdk_test"
capture.psp_TxSource = "WEB"
capture.psp_MerchTxRef = "ORDER66666-3"
capture.psp_TransactionId_Orig = "2693348"
capture.psp_AmountToCapture = "15050"
capture.psp_PosDateTime = "2019-12-01 12:00:00"

response = nps.capture(capture)

print(resp.psp_ResponseCod)
