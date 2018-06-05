using System;
using NpsSDK;

try{

    RootElement data = new RootElement();

    data.Add("psp_Version", "2.2");
    data.Add("psp_MerchantId", "sdk_test");
    data.Add("psp_PaymentMethodId", "Nzmd7DyGytXXC5PtKwnCsXXuQWHJB9EE");
    data.Add("psp_PaymentMethodTag", "Corporate card");

    ComplexElement pspCardInputDetails = new ComplexElement();
    pspCardInputDetails.Add("ExpirationDate", "2501");
    pspCardInputDetails.Add("HolderName", "JOHN DOE");

    data.Add("psp_CardInputDetails", pspCardInputDetails);

    ComplexElement pspPerson = new ComplexElement();
    pspPerson.Add("FirstName", "John");
    pspPerson.Add("LastName", "Doe");
    pspPerson.Add("MiddleName", "Michael");
    pspPerson.Add("PhoneNumber1", "+1 011 11111111");
    pspPerson.Add("PhoneNumber2", "+1 011 22222222");
    pspPerson.Add("DateOfBirth", "1979-01-12");
    pspPerson.Add("Nationality", "ARG");
    pspPerson.Add("Gender", "M");
    pspPerson.Add("IDNumber", "54111111");
    pspPerson.Add("IDType", "200");

    data.Add("psp_Person", pspPerson);

    ComplexElement pspAddress = new ComplexElement();
    pspAddress.Add("Street", "Av. Collins");
    pspAddress.Add("HouseNumber", "4702");
    pspAddress.Add("AdditionalInfo", "2 A");
    pspAddress.Add("StateProvince", "CABA");
    pspAddress.Add("City", "Buenos Aires");
    pspAddress.Add("Country", "ARG");
    pspAddress.Add("ZipCode", "1425");

    data.Add("psp_Address", pspAddress);
    data.Add("psp_PosDateTime", "2008-01-12 13:05:00");
    RootElement response = npsSdk.UpdatePaymentMethod(data);

}
catch (Exception ex){
    //Code to handle error
}

