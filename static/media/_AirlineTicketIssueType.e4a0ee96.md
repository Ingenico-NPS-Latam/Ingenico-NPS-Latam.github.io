import NpsSDK.NpsSdk;
import NpsSDK.RootElement;
import NpsSDK.ComplexElement;
import NpsSDK.ComplexElementArray;
import NpsSDK.ComplexElementArrayItem;

ComplexElement airlineTicketIssue = response.getComplexElement("AirlineTicketIssue");

airlineTicketIssue.getValue("CarrierCode");
airlineTicketIssue.getValue("TravelAgentCode");
airlineTicketIssue.getValue("TravelAgentName");
airlineTicketIssue.getValue("Date");
airlineTicketIssue.getValue("Country");
airlineTicketIssue.getValue("City");
airlineTicketIssue.getValue("Address");
