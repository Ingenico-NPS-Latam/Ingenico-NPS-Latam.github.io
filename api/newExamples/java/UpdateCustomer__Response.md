import NpsSDK.NpsSdk;
import NpsSDK.RootElement;
import NpsSDK.ComplexElement;
import NpsSDK.ComplexElementArray;
import NpsSDK.ComplexElementArrayItem;

RootElement response = npsSdk.updateCustomer(data);

response.getValue("psp_ResponseCod");
response.getValue("psp_ResponseMsg");
response.getValue("psp_MerchantId");
response.getValue("psp_CustomerId");
response.getValue("psp_EmailAddress");
response.getValue("psp_AlternativeEmailAddress");
response.getValue("psp_AccountID");
response.getValue("psp_AccountCreatedAt");

ComplexElement pspPerson = response.getComplexElement("psp_Person");
pspPerson.getValue("FirstName");
pspPerson.getValue("LastName");
pspPerson.getValue("MiddleName");
pspPerson.getValue("PhoneNumber1");
pspPerson.getValue("PhoneNumber2");
pspPerson.getValue("Gender");
pspPerson.getValue("DateOfBirth");
pspPerson.getValue("Nationality");
pspPerson.getValue("IDNumber");
pspPerson.getValue("IDType");


ComplexElement pspAddress = response.getComplexElement("psp_Address");
pspAddress.getValue("Street");
pspAddress.getValue("HouseNumber");
pspAddress.getValue("AdditionalInfo");
pspAddress.getValue("City");
pspAddress.getValue("StateProvince");
pspAddress.getValue("Country");
pspAddress.getValue("ZipCode");

response.getValue("psp_DefaultPaymentMethodId");

List<ComplexElementArrayItem> pspPaymentMethods = response.getComplexElementArray('psp_PaymentMethods');

ComplexElementArrayItem pspPaymentMethods1 = pspPaymentMethods.getValue(1);
pspPaymentMethods1.getValue("PaymentMethodId");
pspPaymentMethods1.getValue("Product");

ComplexElement cardOutputDetails = pspPaymentMethods1.getComplexElement("CardOutputDetails");
cardOutputDetails.getValue("ExpirationDate");
cardOutputDetails.getValue("ExpirationYear");
cardOutputDetails.getValue("ExpirationMonth");
cardOutputDetails.getValue("HolderName");
cardOutputDetails.getValue("IIN");
cardOutputDetails.getValue("Last4");
cardOutputDetails.getValue("NumberLength");
cardOutputDetails.getValue("MaskedNumber");
cardOutputDetails.getValue("MaskedNumberAlternative");

pspPaymentMethods1.getValue("FingerPrint");
pspPaymentMethods1.getValue("CreatedAt");
pspPaymentMethods1.getValue("UpdatedAt");


response.getValue("psp_PosDateTime");
