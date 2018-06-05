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
    data.add("psp_MerchTxRef", "ORDERX1466Xz-3");
    data.add("psp_MerchOrderId", "ORDERX1466Xz");
    data.add("psp_Amount", "15050");
    data.add("psp_NumPayments", "1");
    data.add("psp_Currency", "032");
    data.add("psp_Country", "ARG");
    data.add("psp_Product", "14");
    data.add("psp_CardNumber", "4507990000000010");
    data.add("psp_CardExpDate", "1912");
    data.add("psp_PosDateTime", "2019-12-01 12:00:00");

    ComplexElement pspBillingDetails = new ComplexElement();
    pspBillingDetails.add("Invoice", "54877555");
    pspBillingDetails.add("InvoiceDate", "2017-10-23");
    pspBillingDetails.add("InvoiceAmount", "15050");
    pspBillingDetails.add("InvoiceCurrency", "032");

    ComplexElement Person = new ComplexElement();
    Person.add("DateOfBirth", "1979-01-12");
    Person.add("FirstName", "John");
    Person.add("Gender", "M");
    Person.add("IDNumber", "54111111");
    Person.add("IDType", "200");
    Person.add("LastName", "Doe");
    Person.add("MiddleName", "Michael");
    Person.add("Nationality", "ARG");
    Person.add("PhoneNumber1", "+1 011 11111111");
    Person.add("PhoneNumber2", "+1 011 22222222");

    pspBillingDetails.add("Person", Person);

    ComplexElement Address = new ComplexElement();
    Address.add("AdditionalInfo", "2 A");
    Address.add("City", "Miami");
    Address.add("Country", "USA");
    Address.add("HouseNumber", "1245");
    Address.add("StateProvince", "Florida");
    Address.add("Street", "Av. Collins");
    Address.add("ZipCode", "33140");

    pspBillingDetails.add("Address", Address);

    data.add("psp_BillingDetails", pspBillingDetails);

    ComplexElement pspShippingDetails = new ComplexElement();
    pspShippingDetails.add("TrackingNumber", "154DDD54DWW11");
    pspShippingDetails.add("Method", "10");
    pspShippingDetails.add("Carrier", "200");
    pspShippingDetails.add("DeliveryDate", "2014-11-20");
    pspShippingDetails.add("FreightAmount", "15000");
    pspShippingDetails.add("GiftMessage", "Happy Birthday!");
    pspShippingDetails.add("GiftWrapping", "1");

    ComplexElement PrimaryRecipient = new ComplexElement();
    PrimaryRecipient.add("DateOfBirth", "1979-01-12");
    PrimaryRecipient.add("FirstName", "John");
    PrimaryRecipient.add("Gender", "M");
    PrimaryRecipient.add("IDNumber", "54111111");
    PrimaryRecipient.add("IDType", "200");
    PrimaryRecipient.add("LastName", "Doe");
    PrimaryRecipient.add("MiddleName", "Michael");
    PrimaryRecipient.add("Nationality", "ARG");
    PrimaryRecipient.add("PhoneNumber1", "+1 011 11111111");
    PrimaryRecipient.add("PhoneNumber2", "+1 011 22222222");

    pspShippingDetails.add("PrimaryRecipient", PrimaryRecipient);

    ComplexElement SecondaryRecipient = new ComplexElement();
    SecondaryRecipient.add("DateOfBirth", "1979-01-12");
    SecondaryRecipient.add("FirstName", "John");
    SecondaryRecipient.add("Gender", "M");
    SecondaryRecipient.add("IDNumber", "54111111");
    SecondaryRecipient.add("IDType", "200");
    SecondaryRecipient.add("LastName", "Doe");
    SecondaryRecipient.add("MiddleName", "Michael");
    SecondaryRecipient.add("Nationality", "ARG");
    SecondaryRecipient.add("PhoneNumber1", "+1 011 11111111");
    SecondaryRecipient.add("PhoneNumber2", "+1 011 22222222");

    pspShippingDetails.add("SecondaryRecipient", SecondaryRecipient);

    ComplexElement Address = new ComplexElement();
    Address.add("AdditionalInfo", "2 A");
    Address.add("City", "Miami");
    Address.add("Country", "USA");
    Address.add("HouseNumber", "1245");
    Address.add("StateProvince", "Florida");
    Address.add("Street", "Av. Collins");
    Address.add("ZipCode", "33140");

    pspShippingDetails.add("Address", Address);

    data.add("psp_ShippingDetails", pspShippingDetails);
    RootElement response = npsSdk.payOnline_2p(data);

} catch (WsdlHandlerException ex) {
    //Code to handle error
}
