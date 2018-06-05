local nps = require("npssdk")
nps.configuration.environment= nps.SANDBOX_ENV
nps.configuration.secret_key = "_YOUR_SECRET_KEY_"


refund = {}

refund.psp_Version = "2.2"
refund.psp_MerchantId = "sdk_test"
refund.psp_TxSource = "WEB"
refund.psp_MerchTxRef = "ORDER66666-3"
refund.psp_TransactionId_Orig = "2693348"
refund.psp_AmountToRefund = "15050"
refund.psp_UserId = "john_doe"
refund.psp_PosDateTime = "2019-12-01 12:00:00"

response = nps.refund(refund)

print(resp.psp_ResponseCod)
