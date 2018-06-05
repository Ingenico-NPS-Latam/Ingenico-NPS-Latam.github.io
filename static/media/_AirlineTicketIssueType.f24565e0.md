using System;
using NpsSDK;

ComplexElement AirlineTicketIssue = response.GetComplexElement("AirlineTicketIssue");

airlineTicketIssue.GetValue("CarrierCode");
airlineTicketIssue.GetValue("TravelAgentCode");
airlineTicketIssue.GetValue("TravelAgentName");
airlineTicketIssue.GetValue("Date");
airlineTicketIssue.GetValue("Country");
airlineTicketIssue.GetValue("City");
airlineTicketIssue.GetValue("Address");
