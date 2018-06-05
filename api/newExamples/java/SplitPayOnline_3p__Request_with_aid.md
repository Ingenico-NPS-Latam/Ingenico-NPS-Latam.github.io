import NpsSDK.NpsSdk;
import NpsSDK.RootElement;
import NpsSDK.ComplexElement;
import NpsSDK.ComplexElementArray;
import NpsSDK.ComplexElementArrayItem;

try {

    RootElement data = new RootElement();

    data.add("psp_Version", "2.2");
    data.add("psp_MerchantId", "sdk_test");
    data.add("psp_TxSource", "WEB");
    data.add("psp_MerchOrderId", "ORDER66666");
    data.add("psp_ReturnURL", "http://localhost/");
    data.add("psp_FrmLanguage", "es_AR");
    data.add("psp_Amount", "15050");
    data.add("psp_Currency", "032");
    data.add("psp_Country", "ARG");
    data.add("psp_Product", "14");
    data.add("psp_PosDateTime", "2019-12-01 12:00:00");

    ComplexElementArray pspTransactions = new ComplexElementArray();

    ComplexElementArrayItem pspTransactions1 = new ComplexElementArrayItem();
    pspTransactions1.add("psp_MerchantId", "sdk_test");
    pspTransactions1.add("psp_MerchTxRef", "ORDER66666-10");
    pspTransactions1.add("psp_Product", "14");
    pspTransactions1.add("psp_Amount", "10000");
    pspTransactions1.add("psp_NumPayments", "1");

    pspTransactions.add(pspTransactions1);

    ComplexElementArrayItem pspTransactions2 = new ComplexElementArrayItem();
    pspTransactions2.add("psp_MerchantId", "sdk_test");
    pspTransactions2.add("psp_MerchTxRef", "ORDER66666-11");
    pspTransactions2.add("psp_Product", "14");
    pspTransactions2.add("psp_Amount", "5050");
    pspTransactions2.add("psp_NumPayments", "1");

    pspTransactions.add(pspTransactions2);

    data.add("psp_Transactions", pspTransactions);

    ComplexElement pspAirlineDetails = new ComplexElement();
    pspAirlineDetails.add("PNR", "154DDD54DWW11");

    ComplexElementArray Passengers = new ComplexElementArray();

    ComplexElementArrayItem Passengers1 = new ComplexElementArrayItem();
    Passengers1.add("FirstName", "John");
    Passengers1.add("LastName", "Doe");
    Passengers1.add("MiddleName", "Michael");
    Passengers1.add("Type", "A");
    Passengers1.add("DateOfBirth", "1979-01-12");
    Passengers1.add("Nationality", "ARG");
    Passengers1.add("IDNumber", "54111111");
    Passengers1.add("IDType", "100");
    Passengers1.add("IDCountry", "ARG");
    Passengers1.add("LoyaltyNumber", "254587547");
    Passengers1.add("LoyaltyTier", "1");

    Passengers.add(Passengers1);

    pspAirlineDetails.add("Passengers", Passengers);

    ComplexElement Ticket = new ComplexElement();
    Ticket.add("TicketNumber", "07411865255578");
    Ticket.add("Eticket", "1");
    Ticket.add("Restricted", "1");

    ComplexElement Issue = new ComplexElement();
    Issue.add("TravelAgentCode", "32165464");
    Issue.add("TravelAgentName", "Washington Hilton");
    Issue.add("Date", "2017-01-10");
    Issue.add("Country", "ARG");
    Issue.add("City", "Buenos Aires");
    Issue.add("Address", "Av. Rivadavia 1111");

    Ticket.add("Issue", Issue);
    Ticket.add("TotalFareAmount", "80000");
    Ticket.add("TotalTaxAmount", "25200");
    Ticket.add("TotalFeeAmount", "14800");

    pspAirlineDetails.add("Ticket", Ticket);

    data.add("psp_AirlineDetails", pspAirlineDetails);
    RootElement response = npsSdk.splitPayOnline_3p(data);

} catch (WsdlHandlerException ex) {
    //Code to handle error
}
