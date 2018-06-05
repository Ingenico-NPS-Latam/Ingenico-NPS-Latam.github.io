using System;
using NpsSDK;

RootElement response = npsSdk.UpdateCustomer(data);

response.GetValue("psp_ResponseCod");
response.GetValue("psp_ResponseMsg");
response.GetValue("psp_MerchantId");
response.GetValue("psp_CustomerId");
response.GetValue("psp_EmailAddress");
response.GetValue("psp_AlternativeEmailAddress");
response.GetValue("psp_AccountID");
response.GetValue("psp_AccountCreatedAt");

ComplexElement pspPerson = response.GetComplexElement("psp_Person");
pspPerson.GetValue("FirstName");
pspPerson.GetValue("LastName");
pspPerson.GetValue("MiddleName");
pspPerson.GetValue("PhoneNumber1");
pspPerson.GetValue("PhoneNumber2");
pspPerson.GetValue("Gender");
pspPerson.GetValue("DateOfBirth");
pspPerson.GetValue("Nationality");
pspPerson.GetValue("IDNumber");
pspPerson.GetValue("IDType");


ComplexElement pspAddress = response.GetComplexElement("psp_Address");
pspAddress.GetValue("Street");
pspAddress.GetValue("HouseNumber");
pspAddress.GetValue("AdditionalInfo");
pspAddress.GetValue("City");
pspAddress.GetValue("StateProvince");
pspAddress.GetValue("Country");
pspAddress.GetValue("ZipCode");

response.GetValue("psp_DefaultPaymentMethodId");

ComplexElementArray pspPaymentMethods = response.GetComplexElementArray("psp_PaymentMethods");

ComplexElementArrayItem pspPaymentMethods1 = pspPaymentMethods[1];
pspPaymentMethods1.GetValue("PaymentMethodId");
pspPaymentMethods1.GetValue("Product");

ComplexElement cardOutputDetails = pspPaymentMethods1.GetComplexElement("CardOutputDetails");
cardOutputDetails.GetValue("ExpirationDate");
cardOutputDetails.GetValue("ExpirationYear");
cardOutputDetails.GetValue("ExpirationMonth");
cardOutputDetails.GetValue("HolderName");
cardOutputDetails.GetValue("IIN");
cardOutputDetails.GetValue("Last4");
cardOutputDetails.GetValue("NumberLength");
cardOutputDetails.GetValue("MaskedNumber");
cardOutputDetails.GetValue("MaskedNumberAlternative");

pspPaymentMethods1.GetValue("FingerPrint");
pspPaymentMethods1.GetValue("CreatedAt");
pspPaymentMethods1.GetValue("UpdatedAt");


response.GetValue("psp_PosDateTime");
