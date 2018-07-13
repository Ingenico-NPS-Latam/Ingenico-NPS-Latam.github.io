RootElement data = new RootElement();

data.add("TicketNumber", "07411865255578");
data.add("Eticket", "1");
data.add("Restricted", "1");

ComplexElement Issue = new ComplexElement();
Issue.add("CarrierCode", "AA");
Issue.add("TravelAgentCode", "32165464");
Issue.add("TravelAgentName", "Washington Hilton");
Issue.add("Date", "2017-01-10");
Issue.add("Country", "ARG");
Issue.add("City", "Buenos Aires");
Issue.add("Address", "Av. Rivadavia 1111");

data.add("Issue", Issue);
data.add("TotalFareAmount", "80000");
data.add("TotalTaxAmount", "25200");
data.add("TotalFeeAmount", "14800");
