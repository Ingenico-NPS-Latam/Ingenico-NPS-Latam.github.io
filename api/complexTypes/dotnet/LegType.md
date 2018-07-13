RootElement data = new RootElement();


ComplexElement Leg = new ComplexElement();
Leg.Add("DepartureAirport", "EZE");
Leg.Add("DepartureDatetime", "2014-05-12 13:05:00");
Leg.Add("DepartureAirportTimezone", "-03:00");
Leg.Add("ArrivalAirport", "AMS");
Leg.Add("CarrierCode", "KL");
Leg.Add("FlightNumber", "842");
Leg.Add("FareBasisCode", "HL7LNR");
Leg.Add("FareClassCode", "FR");
Leg.Add("BaseFare", "30000");
Leg.Add("BaseFareCurrency", "032");

data.Add("Leg", Leg);
