local nps = require("npssdk")
nps.configuration.environment= nps.SANDBOX_ENV
nps.configuration.secret_key = "_YOUR_SECRET_KEY_"


payonline3p = {}

payonline3p.psp_Version = "2.2"
payonline3p.psp_MerchantId = "sdk_test"
payonline3p.psp_TxSource = "WEB"
payonline3p.psp_MerchTxRef = "ORDER76666-3"
payonline3p.psp_MerchOrderId = "ORDER76666"
payonline3p.psp_ReturnURL = "http://localhost/"
payonline3p.psp_FrmLanguage = "es_AR"
payonline3p.psp_Amount = "1220000"
payonline3p.psp_NumPayments = "1"
payonline3p.psp_Currency = "858"
payonline3p.psp_Country = "URY"
payonline3p.psp_Product = "5"
payonline3p.psp_PosDateTime = "2019-12-01 12:00:00"

pspAmountAdditionalDetails = {}
pspAmountAdditionalDetails.Tip = "20"
pspAmountAdditionalDetails.Discount = "1"

Taxes = {}

Taxes1 = {}
Taxes1.TypeId = "601"
Taxes1.Amount = "220000"
Taxes1.Rate = "2200"
Taxes1.BaseAmount = "1000000"

Taxes[#Taxes+1] = Taxes1

pspAmountAdditionalDetails.Taxes = Taxes

payonline3p.psp_AmountAdditionalDetails = pspAmountAdditionalDetails

pspBillingDetails = {}
pspBillingDetails.Invoice = "A00024144"
pspBillingDetails.InvoiceAmount = "1600000"
pspBillingDetails.InvoiceCurrency = "858"

payonline3p.psp_BillingDetails = pspBillingDetails

response = nps.pay_online_3p(payonline3p)

print(resp.psp_ResponseCod)
