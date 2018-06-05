local nps = require("npssdk")
nps.configuration.environment= nps.SANDBOX_ENV
nps.configuration.secret_key = "_YOUR_SECRET_KEY_"


amountDetailsRequestType.md = {}


AmountDetailsRequest = {}
AmountDetailsRequest.Tip = "500"
AmountDetailsRequest.Discount = "10000"

Taxes = {}

Taxes1 = {}
Taxes1.TypeId = "500"
Taxes1.Amount = "10000"
Taxes1.Rate = "2100"
Taxes1.BaseAmount = "10000"

Taxes[#Taxes+1] = Taxes1

Taxes2 = {}
Taxes2.TypeId = "500"
Taxes2.Amount = "10000"
Taxes2.Rate = "2100"
Taxes2.BaseAmount = "10000"

Taxes[#Taxes+1] = Taxes2

AmountDetailsRequest.Taxes = Taxes

amountDetailsRequestType.md.AmountDetailsRequest = AmountDetailsRequest

resp = nps.AmountDetailsRequestType.md(amountDetailsRequestType.md)

print(resp.psp_ResponseCod)