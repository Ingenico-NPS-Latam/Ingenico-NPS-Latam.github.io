import NpsSDK.NpsSdk;
import NpsSDK.RootElement;
import NpsSDK.ComplexElement;
import NpsSDK.ComplexElementArray;
import NpsSDK.ComplexElementArrayItem;

ComplexElement airlineDetails = response.getComplexElement("AirlineDetails");

airlineDetails.getValue("name");

ComplexElement values = airlineDetails.getComplexElement("values");
values.getValue("PNR");

List<ComplexElementArrayItem> legs = values.getComplexElementArray('Legs');

ComplexElementArrayItem legs1 = legs.getValue(1);
legs1.getValue("DepartureAirport");
legs1.getValue("DepartureDatetime");
legs1.getValue("DepartureAirportTimezone");
legs1.getValue("ArrivalAirport");
legs1.getValue("CarrierCode");
legs1.getValue("FlightNumber");
legs1.getValue("FareBasisCode");
legs1.getValue("FareClassCode");
legs1.getValue("BaseFare");
legs1.getValue("BaseFareCurrency");



List<ComplexElementArrayItem> passengers = values.getComplexElementArray('Passengers');

ComplexElementArrayItem passengers1 = passengers.getValue(1);
passengers1.getValue("FirstName");
passengers1.getValue("LastName");
passengers1.getValue("MiddleName");
passengers1.getValue("Type");
passengers1.getValue("DateOfBirth");
passengers1.getValue("Nationality");
passengers1.getValue("IDNumber");
passengers1.getValue("IDType");
passengers1.getValue("IDCountry");
passengers1.getValue("LoyaltyNumber");
passengers1.getValue("LoyaltyTier");



ComplexElement ticket = values.getComplexElement("Ticket");
ticket.getValue("TicketNumber");
ticket.getValue("Eticket");
ticket.getValue("Restricted");

ComplexElement issue = Ticket.getComplexElement("Issue");
issue.getValue("CarrierCode");
issue.getValue("TravelAgentCode");
issue.getValue("TravelAgentName");
issue.getValue("Date");
issue.getValue("Country");
issue.getValue("City");
issue.getValue("Address");

ticket.getValue("TotalFareAmount");
ticket.getValue("TotalTaxAmount");
ticket.getValue("TotalFeeAmount");


