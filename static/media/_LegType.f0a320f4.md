import NpsSDK.NpsSdk;
import NpsSDK.RootElement;
import NpsSDK.ComplexElement;
import NpsSDK.ComplexElementArray;
import NpsSDK.ComplexElementArrayItem;

ComplexElement leg = response.getComplexElement("Leg");


ComplexElement leg = leg.getComplexElement("Leg");
leg.getValue("DepartureAirport");
leg.getValue("DepartureDatetime");
leg.getValue("DepartureAirportTimezone");
leg.getValue("ArrivalAirport");
leg.getValue("CarrierCode");
leg.getValue("FlightNumber");
leg.getValue("FareBasisCode");
leg.getValue("FareClassCode");
leg.getValue("BaseFare");
leg.getValue("BaseFareCurrency");

