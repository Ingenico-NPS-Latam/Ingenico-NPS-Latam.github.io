local nps = require("npssdk")
nps.configuration.environment= nps.SANDBOX_ENV
nps.configuration.secret_key = "_YOUR_SECRET_KEY_"


createclientsession = {}

createclientsession.psp_Version = "2.2"
createclientsession.psp_MerchantId = "sdk_test"
createclientsession.psp_PosDateTime = "2019-12-01 12:00:00"
createclientsession.psp_CustomerId = "K8sj5rBrGqPBczTR4LtuKE6g4iZMmY9f"

response = nps.create_client_session(createclientsession)

print(resp.psp_ResponseCod)
