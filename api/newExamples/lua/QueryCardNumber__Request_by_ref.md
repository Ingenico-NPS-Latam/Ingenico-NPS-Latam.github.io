local nps = require("npssdk")
nps.configuration.environment= nps.SANDBOX_ENV
nps.configuration.secret_key = "_YOUR_SECRET_KEY_"


querycardnumber = {}

querycardnumber.psp_Version = "1"
querycardnumber.psp_MerchantId = "sdk_test"
querycardnumber.psp_QueryCriteria = "M"
querycardnumber.psp_QueryCriteriaId = "ORDERX1466Xz-3"
querycardnumber.psp_PosDateTime = "2019-12-01 12:00:00"

response = nps.query_card_number(querycardnumber)

print(resp.psp_ResponseCod)
