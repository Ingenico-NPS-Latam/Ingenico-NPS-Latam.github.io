RootElement data = new RootElement();

data.Add("PNR", "154DDD54DWW11");

ComplexElementArray Legs = new ComplexElementArray();

ComplexElementArrayItem Legs1 = new ComplexElementArrayItem();
Legs1.Add("DepartureAirport", "EZE");
Legs1.Add("DepartureDatetime", "2014-05-12 13:05:00");
Legs1.Add("DepartureAirportTimezone", "-03:00");
Legs1.Add("ArrivalAirport", "AMS");
Legs1.Add("CarrierCode", "KL");
Legs1.Add("FlightNumber", "842");
Legs1.Add("FareBasisCode", "HL7LNR");
Legs1.Add("FareClassCode", "FR");
Legs1.Add("BaseFare", "30000");
Legs1.Add("BaseFareCurrency", "032");

Legs.Add(Legs1);

data.Add("Legs", Legs);

ComplexElementArray Passengers = new ComplexElementArray();

ComplexElementArrayItem Passengers1 = new ComplexElementArrayItem();
Passengers1.Add("FirstName", "John");
Passengers1.Add("LastName", "Doe");
Passengers1.Add("MiddleName", "Michael");
Passengers1.Add("Type", "A");
Passengers1.Add("DateOfBirth", "1979-01-12");
Passengers1.Add("Nationality", "ARG");
Passengers1.Add("IDNumber", "54111111");
Passengers1.Add("IDType", "100");
Passengers1.Add("IDCountry", "ARG");
Passengers1.Add("LoyaltyNumber", "254587547");
Passengers1.Add("LoyaltyTier", "1");

Passengers.Add(Passengers1);

data.Add("Passengers", Passengers);

ComplexElement Ticket = new ComplexElement();
Ticket.Add("TicketNumber", "07411865255578");
Ticket.Add("Eticket", "1");
Ticket.Add("Restricted", "1");

ComplexElement Issue = new ComplexElement();
Issue.Add("CarrierCode", "AA");
Issue.Add("TravelAgentCode", "32165464");
Issue.Add("TravelAgentName", "Washington Hilton");
Issue.Add("Date", "2017-01-10");
Issue.Add("Country", "ARG");
Issue.Add("City", "Buenos Aires");
Issue.Add("Address", "Av. Rivadavia 1111");

Ticket.Add("Issue", Issue);
Ticket.Add("TotalFareAmount", "80000");
Ticket.Add("TotalTaxAmount", "25200");
Ticket.Add("TotalFeeAmount", "14800");

data.Add("Ticket", Ticket);
