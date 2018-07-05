using System;
using NpsSDK;

ComplexElement Leg = response.GetComplexElement("Leg");


ComplexElement leg = Leg.GetComplexElement("Leg");
leg.GetValue("DepartureAirport");
leg.GetValue("DepartureDatetime");
leg.GetValue("DepartureAirportTimezone");
leg.GetValue("ArrivalAirport");
leg.GetValue("CarrierCode");
leg.GetValue("FlightNumber");
leg.GetValue("FareBasisCode");
leg.GetValue("FareClassCode");
leg.GetValue("BaseFare");
leg.GetValue("BaseFareCurrency");

