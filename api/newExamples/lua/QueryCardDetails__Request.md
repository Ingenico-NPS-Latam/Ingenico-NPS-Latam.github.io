local nps = require("npssdk")
nps.configuration.environment= nps.SANDBOX_ENV
nps.configuration.secret_key = "_YOUR_SECRET_KEY_"


querycarddetails = {}

querycarddetails.psp_Version = "2.2"
querycarddetails.psp_MerchantId = "psp_test"
querycarddetails.psp_QueryCriteria = "T"
querycarddetails.psp_QueryCriteriaId = "159744"
querycarddetails.psp_PosDateTime = "2019-12-01 12:00:00"

resp = nps.query_card_details(querycarddetails)

print(resp.psp_ResponseCod)
