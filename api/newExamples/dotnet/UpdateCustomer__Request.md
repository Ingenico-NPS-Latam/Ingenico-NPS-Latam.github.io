using System;
using NpsSDK;

try{

    RootElement data = new RootElement();

    data.Add("psp_Version", "2.2");
    data.Add("psp_MerchantId", "sdk_test");
    data.Add("psp_CustomerId", "bMnVPbNgX55oUz1VLgC41E5iD2rYRo2b");
    data.Add("psp_EmailAddress", "jhon.doe@example.com");
    data.Add("psp_AlternativeEmailAddress", "jdoe@example.com");
    data.Add("psp_AccountCreatedAt", "2010-10-23");
    data.Add("psp_AccountID", "jdoe78");

    ComplexElement pspPerson = new ComplexElement();
    pspPerson.Add("FirstName", "John");
    pspPerson.Add("LastName", "Doe");
    pspPerson.Add("MiddleName", "Michael");
    pspPerson.Add("PhoneNumber1", "+1 011 11111111");
    pspPerson.Add("PhoneNumber2", "+1 011 22222222");
    pspPerson.Add("Gender", "M");
    pspPerson.Add("DateOfBirth", "1979-01-12");
    pspPerson.Add("Nationality", "ARG");
    pspPerson.Add("IDNumber", "54111111");
    pspPerson.Add("IDType", "200");

    data.Add("psp_Person", pspPerson);

    ComplexElement pspAddress = new ComplexElement();
    pspAddress.Add("Street", "Av. Collins");
    pspAddress.Add("HouseNumber", "1245");
    pspAddress.Add("AdditionalInfo", "2 A");
    pspAddress.Add("City", "Miami");
    pspAddress.Add("StateProvince", "Florida");
    pspAddress.Add("Country", "USA");
    pspAddress.Add("ZipCode", "33140");

    data.Add("psp_Address", pspAddress);
    data.Add("psp_PosDateTime", "2008-01-12 13:05:00");
    RootElement response = npsSdk.UpdateCustomer(data);

}
catch (Exception ex){
    //Code to handle error
}

