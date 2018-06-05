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
    data.add("psp_EmailAddress", "jhon.doe@example.com");
    data.add("psp_AlternativeEmailAddress", "jdoe@example.com");
    data.add("psp_AccountCreatedAt", "2010-10-23");
    data.add("psp_AccountID", "jdoe78");

    ComplexElement pspPerson = new ComplexElement();
    pspPerson.add("FirstName", "John");
    pspPerson.add("LastName", "Doe");
    pspPerson.add("MiddleName", "Michael");
    pspPerson.add("PhoneNumber1", "+1 011 11111111");
    pspPerson.add("PhoneNumber2", "+1 011 22222222");
    pspPerson.add("Gender", "M");
    pspPerson.add("DateOfBirth", "1979-01-12");
    pspPerson.add("Nationality", "ARG");
    pspPerson.add("IDNumber", "54111111");
    pspPerson.add("IDType", "200");

    data.add("psp_Person", pspPerson);

    ComplexElement pspAddress = new ComplexElement();
    pspAddress.add("Street", "Av. Collins");
    pspAddress.add("HouseNumber", "1245");
    pspAddress.add("AdditionalInfo", "2 A");
    pspAddress.add("City", "Miami");
    pspAddress.add("StateProvince", "Florida");
    pspAddress.add("Country", "USA");
    pspAddress.add("ZipCode", "33140");

    data.add("psp_Address", pspAddress);
    data.add("psp_PosDateTime", "2008-01-12 13:05:00");
    RootElement response = npsSdk.updateCustomer(data);

} catch (WsdlHandlerException ex) {
    //Code to handle error
}
