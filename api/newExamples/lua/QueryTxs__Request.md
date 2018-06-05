local nps = require("npssdk")
nps.configuration.environment= nps.SANDBOX_ENV
nps.configuration.secret_key = "_YOUR_SECRET_KEY_"


querytxs = {}

querytxs.psp_Version = "2.2"
querytxs.psp_MerchantId = "sdk_test"
querytxs.psp_QueryCriteria = "O"
querytxs.psp_QueryCriteriaId = "ORDER69461-3"
querytxs.psp_PosDateTime = "2019-12-01 12:00:00"

response = nps.query_txs(querytxs)

print(resp.psp_ResponseCod)
