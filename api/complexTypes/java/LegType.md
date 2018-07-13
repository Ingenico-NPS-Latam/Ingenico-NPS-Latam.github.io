RootElement data = new RootElement();


ComplexElement Leg = new ComplexElement();
Leg.add("DepartureAirport", "EZE");
Leg.add("DepartureDatetime", "2014-05-12 13:05:00");
Leg.add("DepartureAirportTimezone", "-03:00");
Leg.add("ArrivalAirport", "AMS");
Leg.add("CarrierCode", "KL");
Leg.add("FlightNumber", "842");
Leg.add("FareBasisCode", "HL7LNR");
Leg.add("FareClassCode", "FR");
Leg.add("BaseFare", "30000");
Leg.add("BaseFareCurrency", "032");

data.add("Leg", Leg);
