using System;
using NpsSDK;

try{

    RootElement data = new RootElement();

    data.Add("psp_Version", "2.2");
    data.Add("psp_MerchantId", "sdk_test");
    data.Add("psp_TxSource", "WEB");
    data.Add("psp_MerchOrderId", "ORDER66666");
    data.Add("psp_ReturnURL", "http://localhost/");
    data.Add("psp_FrmLanguage", "es_AR");
    data.Add("psp_Amount", "15050");
    data.Add("psp_Currency", "032");
    data.Add("psp_Country", "ARG");
    data.Add("psp_Product", "14");
    data.Add("psp_PosDateTime", "2019-12-01 12:00:00");

    ComplexElementArray pspTransactions = new ComplexElementArray();

    ComplexElementArrayItem pspTransactions1 = new ComplexElementArrayItem();
    pspTransactions1.Add("psp_MerchantId", "sdk_test");
    pspTransactions1.Add("psp_MerchTxRef", "ORDER66666-3");
    pspTransactions1.Add("psp_Product", "14");
    pspTransactions1.Add("psp_Amount", "10000");
    pspTransactions1.Add("psp_NumPayments", "1");

    pspTransactions.Add(pspTransactions1);

    ComplexElementArrayItem pspTransactions2 = new ComplexElementArrayItem();
    pspTransactions2.Add("psp_MerchantId", "sdk_test");
    pspTransactions2.Add("psp_MerchTxRef", "ORDER66666-3");
    pspTransactions2.Add("psp_Product", "14");
    pspTransactions2.Add("psp_Amount", "5050");
    pspTransactions2.Add("psp_NumPayments", "1");

    pspTransactions.Add(pspTransactions2);

    data.Add("psp_Transactions", pspTransactions);

    ComplexElement pspAirlineDetails = new ComplexElement();
    pspAirlineDetails.Add("PNR", "154DDD54DWW11");

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

    pspAirlineDetails.Add("Passengers", Passengers);

    ComplexElement Ticket = new ComplexElement();
    Ticket.Add("TicketNumber", "07411865255578");
    Ticket.Add("Eticket", "1");
    Ticket.Add("Restricted", "1");

    ComplexElement Issue = new ComplexElement();
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

    pspAirlineDetails.Add("Ticket", Ticket);

    data.Add("psp_AirlineDetails", pspAirlineDetails);
    RootElement response = npsSdk.SplitAuthorize_3p(data);

}
catch (Exception ex){
    //Code to handle error
}

