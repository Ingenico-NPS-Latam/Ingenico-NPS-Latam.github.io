using System;
using NpsSDK;

try{

    RootElement data = new RootElement();

    data.Add("psp_Version", "2.2");
    data.Add("psp_MerchantId", "sdk_test");
    data.Add("psp_TxSource", "WEB");
    data.Add("psp_MerchTxRef", "ORDER66666-3");
    data.Add("psp_MerchOrderId", "ORDER66666");
    data.Add("psp_Amount", "15050");
    data.Add("psp_NumPayments", "1");
    data.Add("psp_Currency", "032");
    data.Add("psp_Country", "ARG");
    data.Add("psp_Product", "14");
    data.Add("psp_CardNumber", "4507990000000010");
    data.Add("psp_CardExpDate", "1912");
    data.Add("psp_PosDateTime", "2916-12-01 12:00:00");

    ComplexElement pspCustomerAdditionalDetails = new ComplexElement();
    pspCustomerAdditionalDetails.Add("EmailAddress", "jdoe@email.com");
    pspCustomerAdditionalDetails.Add("AlternativeEmailAddress", "Jdoe79@email.com");
    pspCustomerAdditionalDetails.Add("IPAddress", "192.168.158.190");
    pspCustomerAdditionalDetails.Add("AccountID", "Jdoe78");
    pspCustomerAdditionalDetails.Add("AccountCreatedAt", "2010-10-23");
    pspCustomerAdditionalDetails.Add("AccountPreviousActivity", "1");
    pspCustomerAdditionalDetails.Add("AccountHasCredentials", "1");
    pspCustomerAdditionalDetails.Add("DeviceType", "1");
    pspCustomerAdditionalDetails.Add("DeviceFingerPrint", "KJhKHKJgh7777kgh...");
    pspCustomerAdditionalDetails.Add("BrowserLanguage", "ES");
    pspCustomerAdditionalDetails.Add("HttpUserAgent", "Mozilla/5.0 (X11; Ubuntu; Linux x86_64; rv:21.0) Gecko/20100101 Firefox/21.0");

    data.Add("psp_CustomerAdditionalDetails", pspCustomerAdditionalDetails);

    ComplexElement pspBillingDetails = new ComplexElement();
    pspBillingDetails.Add("Invoice", "54877555");
    pspBillingDetails.Add("InvoiceDate", "2017-10-23");
    pspBillingDetails.Add("InvoiceAmount", "15050");
    pspBillingDetails.Add("InvoiceCurrency", "032");

    ComplexElement Person = new ComplexElement();
    Person.Add("DateOfBirth", "1979-01-12");
    Person.Add("FirstName", "John");
    Person.Add("Gender", "M");
    Person.Add("IDNumber", "54111111");
    Person.Add("IDType", "200");
    Person.Add("LastName", "Doe");
    Person.Add("MiddleName", "Michael");
    Person.Add("Nationality", "ARG");
    Person.Add("PhoneNumber1", "+1 011 11111111");
    Person.Add("PhoneNumber2", "+1 011 22222222");

    pspBillingDetails.Add("Person", Person);

    ComplexElement Address = new ComplexElement();
    Address.Add("AdditionalInfo", "2 A");
    Address.Add("City", "Miami");
    Address.Add("Country", "USA");
    Address.Add("HouseNumber", "1245");
    Address.Add("StateProvince", "Florida");
    Address.Add("Street", "Av. Collins");
    Address.Add("ZipCode", "33140");

    pspBillingDetails.Add("Address", Address);

    data.Add("psp_BillingDetails", pspBillingDetails);

    ComplexElement pspAirlineDetails = new ComplexElement();
    pspAirlineDetails.Add("PNR", "154DDD54DWW11");

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

    pspAirlineDetails.Add("Legs", Legs);

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
    RootElement response = npsSdk.FraudScreening(data);

}
catch (Exception ex){
    //Code to handle error
}

