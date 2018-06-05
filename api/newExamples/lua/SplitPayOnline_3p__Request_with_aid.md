local nps = require("npssdk")
nps.configuration.environment= nps.SANDBOX_ENV
nps.configuration.secret_key = "_YOUR_SECRET_KEY_"


splitpayonline3p = {}

splitpayonline3p.psp_Version = "2.2"
splitpayonline3p.psp_MerchantId = "sdk_test"
splitpayonline3p.psp_TxSource = "WEB"
splitpayonline3p.psp_MerchOrderId = "ORDER66666"
splitpayonline3p.psp_ReturnURL = "http://localhost/"
splitpayonline3p.psp_FrmLanguage = "es_AR"
splitpayonline3p.psp_Amount = "15050"
splitpayonline3p.psp_Currency = "032"
splitpayonline3p.psp_Country = "ARG"
splitpayonline3p.psp_Product = "14"
splitpayonline3p.psp_PosDateTime = "2019-12-01 12:00:00"

pspTransactions = {}

pspTransactions1 = {}
pspTransactions1.psp_MerchantId = "sdk_test"
pspTransactions1.psp_MerchTxRef = "ORDER66666-10"
pspTransactions1.psp_Product = "14"
pspTransactions1.psp_Amount = "10000"
pspTransactions1.psp_NumPayments = "1"

pspTransactions[#pspTransactions+1] = pspTransactions1

pspTransactions2 = {}
pspTransactions2.psp_MerchantId = "sdk_test"
pspTransactions2.psp_MerchTxRef = "ORDER66666-11"
pspTransactions2.psp_Product = "14"
pspTransactions2.psp_Amount = "5050"
pspTransactions2.psp_NumPayments = "1"

pspTransactions[#pspTransactions+1] = pspTransactions2

splitpayonline3p.psp_Transactions = pspTransactions

pspAirlineDetails = {}
pspAirlineDetails.PNR = "154DDD54DWW11"

Passengers = {}

Passengers1 = {}
Passengers1.FirstName = "John"
Passengers1.LastName = "Doe"
Passengers1.MiddleName = "Michael"
Passengers1.Type = "A"
Passengers1.DateOfBirth = "1979-01-12"
Passengers1.Nationality = "ARG"
Passengers1.IDNumber = "54111111"
Passengers1.IDType = "100"
Passengers1.IDCountry = "ARG"
Passengers1.LoyaltyNumber = "254587547"
Passengers1.LoyaltyTier = "1"

Passengers[#Passengers+1] = Passengers1

pspAirlineDetails.Passengers = Passengers

Ticket = {}
Ticket.TicketNumber = "07411865255578"
Ticket.Eticket = "1"
Ticket.Restricted = "1"

Issue = {}
Issue.TravelAgentCode = "32165464"
Issue.TravelAgentName = "Washington Hilton"
Issue.Date = "2017-01-10"
Issue.Country = "ARG"
Issue.City = "Buenos Aires"
Issue.Address = "Av. Rivadavia 1111"

Ticket.Issue = Issue
Ticket.TotalFareAmount = "80000"
Ticket.TotalTaxAmount = "25200"
Ticket.TotalFeeAmount = "14800"

pspAirlineDetails.Ticket = Ticket

splitpayonline3p.psp_AirlineDetails = pspAirlineDetails

response = nps.split_pay_online_3p(splitpayonline3p)

print(resp.psp_ResponseCod)
