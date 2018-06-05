local nps = require("npssdk")
nps.configuration.environment= nps.SANDBOX_ENV
nps.configuration.secret_key = "_YOUR_SECRET_KEY_"


cashpayment3p = {}

cashpayment3p.psp_Version = "2.2"
cashpayment3p.psp_MerchantId = "sdk_test"
cashpayment3p.psp_TxSource = "WEB"
cashpayment3p.psp_MerchTxRef = "ORDER32145-3"
cashpayment3p.psp_MerchOrderId = "ORDER32145"
cashpayment3p.psp_ReturnURL = "http://localhost/"
cashpayment3p.psp_FrmLanguage = "es_AR"
cashpayment3p.psp_Amount = "15050"
cashpayment3p.psp_Currency = "032"
cashpayment3p.psp_Country = "ARG"
cashpayment3p.psp_Product = "301"
cashpayment3p.psp_PosDateTime = "2019-12-01 12:00:00"
cashpayment3p.psp_FirstExpDate = "2020-01-01"

response = nps.cash_payment_3p(cashpayment3p)

print(resp.psp_ResponseCod)
