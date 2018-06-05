import NpsSDK.NpsSdk;
import NpsSDK.RootElement;
import NpsSDK.ComplexElement;
import NpsSDK.ComplexElementArray;
import NpsSDK.ComplexElementArrayItem;

try {

    RootElement data = new RootElement();

    data.add("psp_Version", "2.2");
    data.add("psp_MerchantId", "sdk_test");
    data.add("psp_PaymentMethodId", "Nzmd7DyGytXXC5PtKwnCsXXuQWHJB9EE");
    data.add("psp_PaymentMethodTag", "Corporate card");

    ComplexElement pspCardInputDetails = new ComplexElement();
    pspCardInputDetails.add("ExpirationDate", "2501");
    pspCardInputDetails.add("HolderName", "JOHN DOE");

    data.add("psp_CardInputDetails", pspCardInputDetails);

    ComplexElement pspPerson = new ComplexElement();
    pspPerson.add("FirstName", "John");
    pspPerson.add("LastName", "Doe");
    pspPerson.add("MiddleName", "Michael");
    pspPerson.add("PhoneNumber1", "+1 011 11111111");
    pspPerson.add("PhoneNumber2", "+1 011 22222222");
    pspPerson.add("DateOfBirth", "1979-01-12");
    pspPerson.add("Nationality", "ARG");
    pspPerson.add("Gender", "M");
    pspPerson.add("IDNumber", "54111111");
    pspPerson.add("IDType", "200");

    data.add("psp_Person", pspPerson);

    ComplexElement pspAddress = new ComplexElement();
    pspAddress.add("Street", "Av. Collins");
    pspAddress.add("HouseNumber", "4702");
    pspAddress.add("AdditionalInfo", "2 A");
    pspAddress.add("StateProvince", "CABA");
    pspAddress.add("City", "Buenos Aires");
    pspAddress.add("Country", "ARG");
    pspAddress.add("ZipCode", "1425");

    data.add("psp_Address", pspAddress);
    data.add("psp_PosDateTime", "2008-01-12 13:05:00");
    RootElement response = npsSdk.updatePaymentMethod(data);

} catch (WsdlHandlerException ex) {
    //Code to handle error
}
