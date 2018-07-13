RootElement data = new RootElement();

data.Add("TicketNumber", "07411865255578");
data.Add("Eticket", "1");
data.Add("Restricted", "1");

ComplexElement Issue = new ComplexElement();
Issue.Add("CarrierCode", "AA");
Issue.Add("TravelAgentCode", "32165464");
Issue.Add("TravelAgentName", "Washington Hilton");
Issue.Add("Date", "2017-01-10");
Issue.Add("Country", "ARG");
Issue.Add("City", "Buenos Aires");
Issue.Add("Address", "Av. Rivadavia 1111");

data.Add("Issue", Issue);
data.Add("TotalFareAmount", "80000");
data.Add("TotalTaxAmount", "25200");
data.Add("TotalFeeAmount", "14800");
