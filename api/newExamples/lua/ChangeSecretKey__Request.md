local nps = require("npssdk")
nps.configuration.environment= nps.SANDBOX_ENV
nps.configuration.secret_key = "_YOUR_SECRET_KEY_"


changesecretkey = {}

changesecretkey.psp_Version = "2.2"
changesecretkey.psp_MerchantId = "sdk_test"
changesecretkey.psp_NewSecretKey = "YOUR_NEW_SECRET_KEY"
changesecretkey.psp_PosDateTime = "2019-12-01 12:00:00"

response = nps.change_secret_key(changesecretkey)

print(resp.psp_ResponseCod)
