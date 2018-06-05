import NpsSDK.NpsSdk;
import NpsSDK.RootElement;
import NpsSDK.ComplexElement;
import NpsSDK.ComplexElementArray;
import NpsSDK.ComplexElementArrayItem;

try {

    RootElement data = new RootElement();

    data.add("psp_Version", "2.2");
    data.add("psp_MerchantId", "sdk_test");
    data.add("psp_EmailAddress", "jhon.doe@example.com");
    data.add("psp_AlternativeEmailAddress", "jdoe@example.com");
    data.add("psp_AccountID", "jdoe78");
    data.add("psp_AccountCreatedAt", "2010-10-23");

    ComplexElement pspPerson = new ComplexElement();
    pspPerson.add("FirstName", "John");
    pspPerson.add("LastName", "Doe");
    pspPerson.add("MiddleName", "Michael");
    pspPerson.add("PhoneNumber1", "+1 011 11111111");
    pspPerson.add("PhoneNumber2", "+1 011 22222222");
    pspPerson.add("DateOfBirth", "1979-01-12");
    pspPerson.add("Gender", "M");
    pspPerson.add("Nationality", "ARG");
    pspPerson.add("IDNumber", "54111111");
    pspPerson.add("IDType", "200");

    data.add("psp_Person", pspPerson);

    ComplexElement pspAddress = new ComplexElement();
    pspAddress.add("Street", "Av. Collins");
    pspAddress.add("HouseNumber", "1245");
    pspAddress.add("AdditionalInfo", "2 A");
    pspAddress.add("StateProvince", "Florida");
    pspAddress.add("City", "Miami");
    pspAddress.add("Country", "USA");
    pspAddress.add("ZipCode", "33140");

    data.add("psp_Address", pspAddress);

    ComplexElement pspPaymentMethod = new ComplexElement();
    pspPaymentMethod.add("PaymentMethodToken", "KCVMXsbue5fUKOoAxvp1PTJ94gxv2dQM");

    ComplexElement Address = new ComplexElement();
    Address.add("Street", "Av. Collins");
    Address.add("HouseNumber", "1245");
    Address.add("AdditionalInfo", "2 A");
    Address.add("StateProvince", "Florida");
    Address.add("City", "Miami");
    Address.add("Country", "USA");
    Address.add("ZipCode", "33140");

    pspPaymentMethod.add("Address", Address);

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

    data.add("psp_PaymentMethod", pspPaymentMethod);
    data.add("psp_PosDateTime", "2008-01-12 13:05:00");
    RootElement response = npsSdk.createCustomer(data);

} catch (WsdlHandlerException ex) {
    //Code to handle error
}
