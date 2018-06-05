using System;
using NpsSDK;

try{

    RootElement data = new RootElement();

    data.Add("psp_Version", "2.2");
    data.Add("psp_MerchantId", "sdk_test");
    data.Add("psp_CustomerId", "bMnVPbNgX55oUz1VLgC41E5iD2rYRo2b");

    ComplexElement pspPaymentMethod = new ComplexElement();

    ComplexElement CardInputDetails = new ComplexElement();
    CardInputDetails.Add("Number", "4507990000000010");
    CardInputDetails.Add("ExpirationDate", "2501");
    CardInputDetails.Add("SecurityCode", "123");
    CardInputDetails.Add("HolderName", "JOHN DOE");

    pspPaymentMethod.Add("CardInputDetails", CardInputDetails);
    pspPaymentMethod.Add("PaymentMethodTag", "Corporate card");

    ComplexElement Person = new ComplexElement();
    Person.Add("FirstName", "John");
    Person.Add("LastName", "Doe");
    Person.Add("MiddleName", "Michael");
    Person.Add("PhoneNumber1", "+1 011 11111111");
    Person.Add("PhoneNumber2", "+1 011 22222222");
    Person.Add("DateOfBirth", "1979-01-12");
    Person.Add("Gender", "M");
    Person.Add("Nationality", "ARG");
    Person.Add("IDNumber", "54111111");
    Person.Add("IDType", "200");

    pspPaymentMethod.Add("Person", Person);

    ComplexElement Address = new ComplexElement();
    Address.Add("Street", "Av. Collins");
    Address.Add("HouseNumber", "4702");
    Address.Add("AdditionalInfo", "2 A");
    Address.Add("City", "Buenos Aires");
    Address.Add("StateProvince", "CABA");
    Address.Add("Country", "ARG");
    Address.Add("ZipCode", "1425");

    pspPaymentMethod.Add("Address", Address);

    data.Add("psp_PaymentMethod", pspPaymentMethod);
    data.Add("psp_SetAsCustomerDefault", "1");
    data.Add("psp_PosDateTime", "2008-01-12 13:05:00");
    RootElement response = npsSdk.CreatePaymentMethod(data);

}
catch (Exception ex){
    //Code to handle error
}

