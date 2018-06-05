import NpsSDK.NpsSdk;
import NpsSDK.RootElement;
import NpsSDK.ComplexElement;
import NpsSDK.ComplexElementArray;
import NpsSDK.ComplexElementArrayItem;

RootElement response = npsSdk.recachePaymentMethodToken(data);

response.getValue("psp_ResponseCod");
response.getValue("psp_ResponseMsg");
response.getValue("psp_MerchantId");
response.getValue("psp_PaymentMethodToken");
response.getValue("psp_Product");

ComplexElement pspCardOutputDetails = response.getComplexElement("psp_CardOutputDetails");
pspCardOutputDetails.getValue("ExpirationDate");
pspCardOutputDetails.getValue("ExpirationYear");
pspCardOutputDetails.getValue("ExpirationMonth");
pspCardOutputDetails.getValue("HolderName");
pspCardOutputDetails.getValue("IIN");
pspCardOutputDetails.getValue("Last4");
pspCardOutputDetails.getValue("NumberLength");
pspCardOutputDetails.getValue("MaskedNumber");
pspCardOutputDetails.getValue("MaskedNumberAlternative");


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

response.getValue("psp_AlreadyUsed");
response.getValue("psp_CreatedAt");
response.getValue("psp_UpdatedAt");
