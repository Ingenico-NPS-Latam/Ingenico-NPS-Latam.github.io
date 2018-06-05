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
    data.Add("psp_PosDateTime", "2019-12-01 12:00:00");

    ComplexElement pspVaultReference = new ComplexElement();
    pspVaultReference.Add("PaymentMethodId", "Nzmd7DyGytXXC5PtKwnCsXXuQWHJB9EE");

    data.Add("psp_VaultReference", pspVaultReference);

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

    ComplexElement pspShippingDetails = new ComplexElement();
    pspShippingDetails.Add("TrackingNumber", "154DDD54DWW11");
    pspShippingDetails.Add("Method", "99");
    pspShippingDetails.Add("Carrier", "200");
    pspShippingDetails.Add("DeliveryDate", "2014-11-20");
    pspShippingDetails.Add("FreightAmount", "15000");
    pspShippingDetails.Add("GiftMessage", "Happy Birthday!");
    pspShippingDetails.Add("GiftWrapping", "1");

    ComplexElement PrimaryRecipient = new ComplexElement();
    PrimaryRecipient.Add("DateOfBirth", "1979-01-12");
    PrimaryRecipient.Add("FirstName", "John");
    PrimaryRecipient.Add("Gender", "M");
    PrimaryRecipient.Add("IDNumber", "54111111");
    PrimaryRecipient.Add("IDType", "200");
    PrimaryRecipient.Add("LastName", "Doe");
    PrimaryRecipient.Add("MiddleName", "Michael");
    PrimaryRecipient.Add("Nationality", "ARG");
    PrimaryRecipient.Add("PhoneNumber1", "+1 011 11111111");
    PrimaryRecipient.Add("PhoneNumber2", "+1 011 22222222");

    pspShippingDetails.Add("PrimaryRecipient", PrimaryRecipient);

    ComplexElement SecondaryRecipient = new ComplexElement();
    SecondaryRecipient.Add("DateOfBirth", "1979-01-12");
    SecondaryRecipient.Add("FirstName", "John");
    SecondaryRecipient.Add("Gender", "M");
    SecondaryRecipient.Add("IDNumber", "54111111");
    SecondaryRecipient.Add("IDType", "200");
    SecondaryRecipient.Add("LastName", "Doe");
    SecondaryRecipient.Add("MiddleName", "Michael");
    SecondaryRecipient.Add("Nationality", "ARG");
    SecondaryRecipient.Add("PhoneNumber1", "+1 011 11111111");
    SecondaryRecipient.Add("PhoneNumber2", "+1 011 22222222");

    pspShippingDetails.Add("SecondaryRecipient", SecondaryRecipient);

    ComplexElement Address = new ComplexElement();
    Address.Add("AdditionalInfo", "2 A");
    Address.Add("City", "Miami");
    Address.Add("Country", "USA");
    Address.Add("HouseNumber", "1245");
    Address.Add("StateProvince", "Florida");
    Address.Add("Street", "Av. Collins");
    Address.Add("ZipCode", "33140");

    pspShippingDetails.Add("Address", Address);

    data.Add("psp_ShippingDetails", pspShippingDetails);

    ComplexElement pspOrderDetails = new ComplexElement();

    ComplexElementArray OrderItems = new ComplexElementArray();

    ComplexElementArrayItem OrderItems1 = new ComplexElementArrayItem();
    OrderItems1.Add("Quantity", "10");
    OrderItems1.Add("UnitPrice", "10050");
    OrderItems1.Add("Description", "Blue pencil");
    OrderItems1.Add("Type", "1002");
    OrderItems1.Add("SkuCode", "SO-4587885545");
    OrderItems1.Add("ManufacturerPartNumber", "CN-0N2828421-3AD-02CD");
    OrderItems1.Add("Risk", "H");

    OrderItems.Add(OrderItems1);

    pspOrderDetails.Add("OrderItems", OrderItems);

    data.Add("psp_OrderDetails", pspOrderDetails);
    RootElement response = npsSdk.FraudScreening(data);

}
catch (Exception ex){
    //Code to handle error
}

