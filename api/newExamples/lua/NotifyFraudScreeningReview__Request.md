local nps = require("npssdk")
nps.configuration.environment= nps.SANDBOX_ENV
nps.configuration.secret_key = "_YOUR_SECRET_KEY_"


notifyfraudscreeningreview = {}

notifyfraudscreeningreview.psp_Version = "2.2"
notifyfraudscreeningreview.psp_MerchantId = "sdk_test"
notifyfraudscreeningreview.psp_Criteria = "T"
notifyfraudscreeningreview.psp_CriteriaId = "ORDER69461-3"
notifyfraudscreeningreview.psp_ReviewResult = "A"
notifyfraudscreeningreview.psp_PosDateTime = "2019-12-01 12:00:00"

response = nps.notify_fraud_screening_review(notifyfraudscreeningreview)

print(resp.psp_ResponseCod)
