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
    data.add("psp_MerchTxRef", "ORDER66666-3");
    data.add("psp_MerchOrderId", "ORDER66666");
    data.add("psp_Amount", "15050");
    data.add("psp_NumPayments", "1");
    data.add("psp_Currency", "032");
    data.add("psp_Country", "ARG");
    data.add("psp_Product", "14");
    data.add("psp_PosDateTime", "2019-12-01 12:00:00");

    ComplexElement pspVaultReference = new ComplexElement();
    pspVaultReference.add("PaymentMethodId", "Nzmd7DyGytXXC5PtKwnCsXXuQWHJB9EE");

    data.add("psp_VaultReference", pspVaultReference);

    ComplexElement pspCustomerAdditionalDetails = new ComplexElement();
    pspCustomerAdditionalDetails.add("EmailAddress", "jdoe@email.com");
    pspCustomerAdditionalDetails.add("AlternativeEmailAddress", "Jdoe79@email.com");
    pspCustomerAdditionalDetails.add("IPAddress", "192.168.158.190");
    pspCustomerAdditionalDetails.add("AccountID", "Jdoe78");
    pspCustomerAdditionalDetails.add("AccountCreatedAt", "2010-10-23");
    pspCustomerAdditionalDetails.add("AccountPreviousActivity", "1");
    pspCustomerAdditionalDetails.add("AccountHasCredentials", "1");
    pspCustomerAdditionalDetails.add("DeviceType", "1");
    pspCustomerAdditionalDetails.add("DeviceFingerPrint", "KJhKHKJgh7777kgh...");
    pspCustomerAdditionalDetails.add("BrowserLanguage", "ES");
    pspCustomerAdditionalDetails.add("HttpUserAgent", "Mozilla/5.0 (X11; Ubuntu; Linux x86_64; rv:21.0) Gecko/20100101 Firefox/21.0");

    data.add("psp_CustomerAdditionalDetails", pspCustomerAdditionalDetails);

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
    pspShippingDetails.add("Method", "99");
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

    ComplexElement pspOrderDetails = new ComplexElement();

    ComplexElementArray OrderItems = new ComplexElementArray();

    ComplexElementArrayItem OrderItems1 = new ComplexElementArrayItem();
    OrderItems1.add("Quantity", "10");
    OrderItems1.add("UnitPrice", "10050");
    OrderItems1.add("Description", "Blue pencil");
    OrderItems1.add("Type", "1002");
    OrderItems1.add("SkuCode", "SO-4587885545");
    OrderItems1.add("ManufacturerPartNumber", "CN-0N2828421-3AD-02CD");
    OrderItems1.add("Risk", "H");

    OrderItems.add(OrderItems1);

    pspOrderDetails.add("OrderItems", OrderItems);

    data.add("psp_OrderDetails", pspOrderDetails);
    RootElement response = npsSdk.fraudScreening(data);

} catch (WsdlHandlerException ex) {
    //Code to handle error
}
