local nps = require("npssdk")
nps.configuration.environment= nps.SANDBOX_ENV
nps.configuration.secret_key = "_YOUR_SECRET_KEY_"


getiindetails = {}

getiindetails.psp_Version = "2.2"
getiindetails.psp_MerchantId = "sdk_test"
getiindetails.psp_IIN = "424242"
getiindetails.psp_PosDateTime = "2019-12-01 12:00:00"

response = nps.get_iin_details(getiindetails)

print(resp.psp_ResponseCod)
