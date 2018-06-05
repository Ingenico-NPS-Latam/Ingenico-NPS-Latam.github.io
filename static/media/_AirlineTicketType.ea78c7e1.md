using System;
using NpsSDK;

ComplexElement AirlineTicket = response.GetComplexElement("AirlineTicket");

airlineTicket.GetValue("TicketNumber");
airlineTicket.GetValue("Eticket");
airlineTicket.GetValue("Restricted");

ComplexElement issue = AirlineTicket.GetComplexElement("Issue");
issue.GetValue("CarrierCode");
issue.GetValue("TravelAgentCode");
issue.GetValue("TravelAgentName");
issue.GetValue("Date");
issue.GetValue("Country");
issue.GetValue("City");
issue.GetValue("Address");

airlineTicket.GetValue("TotalFareAmount");
airlineTicket.GetValue("TotalTaxAmount");
airlineTicket.GetValue("TotalFeeAmount");
