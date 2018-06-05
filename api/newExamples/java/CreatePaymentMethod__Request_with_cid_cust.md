import NpsSDK.NpsSdk;
import NpsSDK.RootElement;
import NpsSDK.ComplexElement;
import NpsSDK.ComplexElementArray;
import NpsSDK.ComplexElementArrayItem;

try {

    RootElement data = new RootElement();

    data.add("psp_Version", "2.2");
    data.add("psp_MerchantId", "sdk_test");
    data.add("psp_CustomerId", "bMnVPbNgX55oUz1VLgC41E5iD2rYRo2b");

    ComplexElement pspPaymentMethod = new ComplexElement();

    ComplexElement CardInputDetails = new ComplexElement();
    CardInputDetails.add("Number", "4507990000000010");
    CardInputDetails.add("ExpirationDate", "2501");
    CardInputDetails.add("SecurityCode", "123");
    CardInputDetails.add("HolderName", "JOHN DOE");

    pspPaymentMethod.add("CardInputDetails", CardInputDetails);
    pspPaymentMethod.add("PaymentMethodTag", "Corporate card");

    ComplexElement Person = new ComplexElement();
    Person.add("FirstName", "John");
    Person.add("LastName", "Doe");
    Person.add("MiddleName", "Michael");
    Person.add("PhoneNumber1", "+1 011 11111111");
    Person.add("PhoneNumber2", "+1 011 22222222");
    Person.add("DateOfBirth", "1979-01-12");
    Person.add("Gender", "M");
    Person.add("Nationality", "ARG");
    Person.add("IDNumber", "54111111");
    Person.add("IDType", "200");

    pspPaymentMethod.add("Person", Person);

    ComplexElement Address = new ComplexElement();
    Address.add("Street", "Av. Collins");
    Address.add("HouseNumber", "4702");
    Address.add("AdditionalInfo", "2 A");
    Address.add("City", "Buenos Aires");
    Address.add("StateProvince", "CABA");
    Address.add("Country", "ARG");
    Address.add("ZipCode", "1425");

    pspPaymentMethod.add("Address", Address);

    data.add("psp_PaymentMethod", pspPaymentMethod);
    data.add("psp_SetAsCustomerDefault", "1");
    data.add("psp_PosDateTime", "2008-01-12 13:05:00");
    RootElement response = npsSdk.createPaymentMethod(data);

} catch (WsdlHandlerException ex) {
    //Code to handle error
}
