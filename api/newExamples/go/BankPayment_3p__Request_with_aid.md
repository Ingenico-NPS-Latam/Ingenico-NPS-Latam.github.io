package main

import (
    "fmt"
    "github.com/Ingenico-NPS-Latam/nps-sdk-go/npsSdk"
    CONSTANTS "github.com/Ingenico-NPS-Latam/nps-sdk-go/npsSdk/constants"
)

func main() {

err := npsSdk.Configure(map[string]interface{}(
    "environment": CONSTANTS.SANDBOX_ENV,
    "secret_key": "_YOUR_SECRET_KEY_",
    "debug": true,
    "log_level": CONSTANTS.DEBUG,
})

service := npsSdk.NewPaymentServicePlatformPortType(true)

BankPayment3p := npsSdk.NewRequerimientoStruct_BankPayment_3p()

BankPayment3p.Psp_Version = "2.2"
BankPayment3p.Psp_MerchantId = "sdk_test"
BankPayment3p.Psp_TxSource = "WEB"
BankPayment3p.Psp_MerchTxRef = "ORDER66666-3"
BankPayment3p.Psp_MerchOrderId = "ORDER66666"
BankPayment3p.Psp_ReturnURL = "http://localhost/"
BankPayment3p.Psp_FrmLanguage = "es_AR"
BankPayment3p.Psp_ScreenDescription = "Descripcion"
BankPayment3p.Psp_TicketDescription = "Descripcion"
BankPayment3p.Psp_Currency = "032"
BankPayment3p.Psp_Country = "ARG"
BankPayment3p.Psp_Product = "320"
BankPayment3p.Psp_ExpDate1 = "2019-12-01"
BankPayment3p.Psp_Amount1 = "15050"
BankPayment3p.Psp_ExpMark = "0"
BankPayment3p.Psp_ExpTime = "14:00:00"
BankPayment3p.Psp_PosDateTime = "2019-12-01 12:00:00"

pspAirlineDetails := nps.NewAirlineDetailsStruct()
pspAirlineDetails.PNR = "154DDD54DWW11"

Legs := nps.NewArrayOf_LegsStruct()
Legs.Items = make([]*nps.NewLegsStruct(), 0)

Legs1 := nps.NewLegsStruct()
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
Legs.Items = append(Legs.Items, Legs1)


Passengers := nps.NewArrayOf_PassengersStruct()
Passengers.Items = make([]*nps.NewPassengersStruct(), 0)

Passengers1 := nps.NewPassengersStruct()
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
Passengers.Items = append(Passengers.Items, Passengers1)


Ticket := nps.NewTicketStruct()
Ticket.TicketNumber = "07411865255578"
Ticket.Eticket = "1"
Ticket.Restricted = "1"

Issue := nps.NewIssueStruct()
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

BankPayment3p.psp_AirlineDetails = pspAirlineDetails

resp, err := service.BankPayment_3p(BankPayment3p)

if err != nil {
    fmt.Printf("Error: = [%s]", err)
}
fmt.Printf("Response = [%s] [%s]", resp.Psp_ResponseCod, resp.Psp_ResponseMsg)
fmt.Printf("Extended = [%s]", resp.Psp_ResponseExtended)
