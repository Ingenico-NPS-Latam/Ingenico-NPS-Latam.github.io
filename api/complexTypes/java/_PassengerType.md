import NpsSDK.NpsSdk;
import NpsSDK.RootElement;
import NpsSDK.ComplexElement;
import NpsSDK.ComplexElementArray;
import NpsSDK.ComplexElementArrayItem;

ComplexElement passenger = response.getComplexElement("Passenger");


ComplexElement passenger = passenger.getComplexElement("Passenger");
passenger.getValue("FirstName");
passenger.getValue("LastName");
passenger.getValue("MiddleName");
passenger.getValue("Type");
passenger.getValue("DateOfBirth");
passenger.getValue("Nationality");
passenger.getValue("IDNumber");
passenger.getValue("IDType");
passenger.getValue("IDCountry");
passenger.getValue("LoyaltyNumber");
passenger.getValue("LoyaltyTier");

