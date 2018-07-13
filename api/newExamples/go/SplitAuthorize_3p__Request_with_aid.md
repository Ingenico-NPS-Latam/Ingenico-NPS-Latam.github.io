package main

import (
        "fmt"
        "log"
        "npsSdk"
        CONSTANTS "npsSdk/constants"
)

service:= nps.NewPaymentServicePlatformPortType(true)

SplitAuthorize3p := nps.NewRequerimientoStruct_SplitAuthorize_3p()

SplitAuthorize3p.Psp_Version = "2.2"
SplitAuthorize3p.Psp_MerchantId = "sdk_test"
SplitAuthorize3p.Psp_TxSource = "WEB"
SplitAuthorize3p.Psp_MerchOrderId = "ORDER66666"
SplitAuthorize3p.Psp_ReturnURL = "http://localhost/"
SplitAuthorize3p.Psp_FrmLanguage = "es_AR"
SplitAuthorize3p.Psp_Amount = "15050"
SplitAuthorize3p.Psp_Currency = "032"
SplitAuthorize3p.Psp_Country = "ARG"
SplitAuthorize3p.Psp_Product = "14"
SplitAuthorize3p.Psp_PosDateTime = "2019-12-01 12:00:00"

pspTransactions := nps.NewTransactionsStruct()

pspTransactions1 := pspTransactions.Items[1];
pspTransactions1.Psp_MerchantId = "sdk_test"
pspTransactions1.Psp_MerchTxRef = "ORDER66666-3"
pspTransactions1.Psp_Product = "14"
pspTransactions1.Psp_Amount = "10000"
pspTransactions1.Psp_NumPayments = "1"

pspTransactions2 := pspTransactions.Items[2];
pspTransactions2.Psp_MerchantId = "sdk_test"
pspTransactions2.Psp_MerchTxRef = "ORDER66666-3"
pspTransactions2.Psp_Product = "14"
pspTransactions2.Psp_Amount = "5050"
pspTransactions2.Psp_NumPayments = "1"


SplitAuthorize3p.psp_Transactions = pspTransactions

pspAirlineDetails := nps.NewAirlineDetailsStruct()
pspAirlineDetails.PNR = "154DDD54DWW11"

Passengers := nps.NewPassengersStruct()

Passengers1 := Passengers.Items[1];
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


pspAirlineDetails.Passengers = Passengers

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

SplitAuthorize3p.psp_AirlineDetails = pspAirlineDetails

response, err := service.SplitAuthorize_3p(SplitAuthorize3p)

if err != nil {
    fmt.Printf("Error: = [%s]", err)
}
fmt.Printf("Response = [%s] [%s]", resp.Psp_ResponseCod, resp.Psp_ResponseMsg)
fmt.Printf("Extended = [%s]", resp.Psp_ResponseExtended)



