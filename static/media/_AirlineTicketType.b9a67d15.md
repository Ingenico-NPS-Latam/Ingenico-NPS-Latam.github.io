import NpsSDK.NpsSdk;
import NpsSDK.RootElement;
import NpsSDK.ComplexElement;
import NpsSDK.ComplexElementArray;
import NpsSDK.ComplexElementArrayItem;

ComplexElement airlineTicket = response.getComplexElement("AirlineTicket");

airlineTicket.getValue("TicketNumber");
airlineTicket.getValue("Eticket");
airlineTicket.getValue("Restricted");

ComplexElement issue = airlineTicket.getComplexElement("Issue");
issue.getValue("CarrierCode");
issue.getValue("TravelAgentCode");
issue.getValue("TravelAgentName");
issue.getValue("Date");
issue.getValue("Country");
issue.getValue("City");
issue.getValue("Address");

airlineTicket.getValue("TotalFareAmount");
airlineTicket.getValue("TotalTaxAmount");
airlineTicket.getValue("TotalFeeAmount");
