import NpsSDK.NpsSdk;
import NpsSDK.RootElement;
import NpsSDK.ComplexElement;
import NpsSDK.ComplexElementArray;
import NpsSDK.ComplexElementArrayItem;

try {

    RootElement data = new RootElement();

    data.add("psp_Version", "2.2");
    data.add("psp_MerchantId", "sdk_test");

    ComplexElement pspCardInputDetails = new ComplexElement();
    pspCardInputDetails.add("Number", "4507990000000010");
    pspCardInputDetails.add("ExpirationDate", "2501");
    pspCardInputDetails.add("SecurityCode", "123");
    pspCardInputDetails.add("HolderName", "JOHN DOE");

    data.add("psp_CardInputDetails", pspCardInputDetails);

    ComplexElement pspPerson = new ComplexElement();
    pspPerson.add("FirstName", "John");
    pspPerson.add("LastName", "Doe");
    pspPerson.add("MiddleName", "Michael");
    pspPerson.add("DateOfBirth", "1979-01-12");
    pspPerson.add("PhoneNumber1", "+1 011 11111111");
    pspPerson.add("PhoneNumber2", "+1 011 22222222");
    pspPerson.add("Gender", "M");
    pspPerson.add("Nationality", "ARG");
    pspPerson.add("IDNumber", "54111111");
    pspPerson.add("IDType", "200");

    data.add("psp_Person", pspPerson);

    ComplexElement pspAddress = new ComplexElement();
    pspAddress.add("Street", "Av. Collins");
    pspAddress.add("HouseNumber", "4702");
    pspAddress.add("AdditionalInfo", "2 A");
    pspAddress.add("City", "Buenos Aires");
    pspAddress.add("StateProvince", "CABA");
    pspAddress.add("Country", "ARG");
    pspAddress.add("ZipCode", "1425");

    data.add("psp_Address", pspAddress);
    data.add("psp_ClientSession", "C5jwwbyAYneLbvZe0IYPHTvn7ODMb3vG8ZqCYaYIioUmWUbcgKscGpg8WhXrspRs");
    RootElement response = npsSdk.createPaymentMethodToken(data);

} catch (WsdlHandlerException ex) {
    //Code to handle error
}
