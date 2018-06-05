local nps = require("npssdk")
nps.configuration.environment= nps.SANDBOX_ENV
nps.configuration.secret_key = "_YOUR_SECRET_KEY_"


bankpayment3p = {}

bankpayment3p.psp_Version = "2.2"
bankpayment3p.psp_MerchantId = "sdk_test"
bankpayment3p.psp_TxSource = "WEB"
bankpayment3p.psp_MerchTxRef = "ORDER66666-3"
bankpayment3p.psp_MerchOrderId = "ORDER66666"
bankpayment3p.psp_ReturnURL = "http://localhost/"
bankpayment3p.psp_FrmLanguage = "es_AR"
bankpayment3p.psp_ScreenDescription = "Descripcion"
bankpayment3p.psp_TicketDescription = "Descripcion"
bankpayment3p.psp_Currency = "032"
bankpayment3p.psp_Country = "ARG"
bankpayment3p.psp_Product = "320"
bankpayment3p.psp_ExpDate1 = "2019-12-01"
bankpayment3p.psp_Amount1 = "15050"
bankpayment3p.psp_ExpMark = "0"
bankpayment3p.psp_ExpTime = "14:00:00"
bankpayment3p.psp_PosDateTime = "2019-12-01 12:00:00"

response = nps.bank_payment_3p(bankpayment3p)

print(resp.psp_ResponseCod)
