local nps = require("npssdk")
nps.configuration.environment= nps.SANDBOX_ENV
nps.configuration.secret_key = "_YOUR_SECRET_KEY_"


simplequerytx = {}

simplequerytx.psp_Version = "2.2"
simplequerytx.psp_MerchantId = "sdk_test"
simplequerytx.psp_QueryCriteria = "T"
simplequerytx.psp_QueryCriteriaId = "2693310"
simplequerytx.psp_PosDateTime = "2019-12-01 12:00:00"

response = nps.simple_query_tx(simplequerytx)

print(resp.psp_ResponseCod)
