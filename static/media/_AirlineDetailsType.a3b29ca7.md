using System;
using NpsSDK;

ComplexElement AirlineDetails = response.GetComplexElement("AirlineDetails");

airlineDetails.GetValue("name");

ComplexElement values = AirlineDetails.GetComplexElement("values");
values.GetValue("PNR");

ComplexElementArray legs = values.GetComplexElementArray("Legs");

ComplexElementArrayItem legs1 = legs[1];
legs1.GetValue("DepartureAirport");
legs1.GetValue("DepartureDatetime");
legs1.GetValue("DepartureAirportTimezone");
legs1.GetValue("ArrivalAirport");
legs1.GetValue("CarrierCode");
legs1.GetValue("FlightNumber");
legs1.GetValue("FareBasisCode");
legs1.GetValue("FareClassCode");
legs1.GetValue("BaseFare");
legs1.GetValue("BaseFareCurrency");



ComplexElementArray passengers = values.GetComplexElementArray("Passengers");

ComplexElementArrayItem passengers1 = passengers[1];
passengers1.GetValue("FirstName");
passengers1.GetValue("LastName");
passengers1.GetValue("MiddleName");
passengers1.GetValue("Type");
passengers1.GetValue("DateOfBirth");
passengers1.GetValue("Nationality");
passengers1.GetValue("IDNumber");
passengers1.GetValue("IDType");
passengers1.GetValue("IDCountry");
passengers1.GetValue("LoyaltyNumber");
passengers1.GetValue("LoyaltyTier");



ComplexElement ticket = values.GetComplexElement("Ticket");
ticket.GetValue("TicketNumber");
ticket.GetValue("Eticket");
ticket.GetValue("Restricted");

ComplexElement issue = Ticket.GetComplexElement("Issue");
issue.GetValue("CarrierCode");
issue.GetValue("TravelAgentCode");
issue.GetValue("TravelAgentName");
issue.GetValue("Date");
issue.GetValue("Country");
issue.GetValue("City");
issue.GetValue("Address");

ticket.GetValue("TotalFareAmount");
ticket.GetValue("TotalTaxAmount");
ticket.GetValue("TotalFeeAmount");


