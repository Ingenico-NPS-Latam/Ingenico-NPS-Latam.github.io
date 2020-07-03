local nps = require("npssdk")
nps.configuration.environment= nps.SANDBOX_ENV
nps.configuration.secret_key = "_YOUR_SECRET_KEY_"


authorize2p = {}

authorize2p.psp_Version = "2.2"
authorize2p.psp_MerchantId = "sdk_test"
authorize2p.psp_TxSource = "WEB"
authorize2p.psp_MerchTxRef = "ORDERX1466Xz-3"
authorize2p.psp_MerchOrderId = "ORDERX1466Xz"
authorize2p.psp_Amount = "15050"
authorize2p.psp_NumPayments = "1"
authorize2p.psp_Currency = "032"
authorize2p.psp_Country = "ARG"
authorize2p.psp_Product = "14"
authorize2p.psp_CardNumber = "4507990000000010"
authorize2p.psp_CardExpDate = "1912"
authorize2p.psp_PosDateTime = "2019-12-01 12:00:00"
authorize2p.psp_3dSecure_XID = "MjY0MjAxNjA4MDIyMDUzMzYyNjU="
authorize2p.psp_3dSecure_CAVV = "AAABBYZ3N5Qhl3kBU3c3ELGUsMY="
authorize2p.psp_3dSecure_ECI = "05"
authorize2p.psp_3dSecure_Secured = "1"
authorize2p.psp_3dSecure_ProtocolVersion = "2.1.0"
authorize2p.psp_3dSecure_DirectoryServerTransactionId = "c4e59ceb-a382-4d6a-bc87-385d591fa09d"

response = nps.authorize_2p(authorize2p)

print(resp.psp_ResponseCod)
