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

pspAirlineDetails = {}
pspAirlineDetails.PNR = "154DDD54DWW11"

Legs = {}

Legs1 = {}
Legs1.DepartureAirport = "EZE"
Legs1.DepartureDatetime = "2014-05-12 13:05:00"
Legs1.DepartureAirportTimezone = "-03:00"
Legs1.ArrivalAirport = "AMS"
Legs1.CarrierCode = "KL"
Legs1.FlightNumber = "842"
Legs1.FareBasisCode = "HL7LNR"
Legs1.FareClassCode = "FR"
Legs1.BaseFare = "30000"
Legs1.BaseFareCurrency = "032"

Legs[#Legs+1] = Legs1

pspAirlineDetails.Legs = Legs

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

bankpayment3p.psp_AirlineDetails = pspAirlineDetails

response = nps.bank_payment_3p(bankpayment3p)

print(resp.psp_ResponseCod)
