using System;
using NpsSDK;

RootElement response = npsSdk.RetrievePaymentMethodToken(data);

response.GetValue("psp_ResponseCod");
response.GetValue("psp_ResponseMsg");
response.GetValue("psp_MerchantId");
response.GetValue("psp_PaymentMethodToken");
response.GetValue("psp_Product");

ComplexElement pspCardOutputDetails = response.GetComplexElement("psp_CardOutputDetails");
pspCardOutputDetails.GetValue("ExpirationDate");
pspCardOutputDetails.GetValue("ExpirationYear");
pspCardOutputDetails.GetValue("ExpirationMonth");
pspCardOutputDetails.GetValue("HolderName");
pspCardOutputDetails.GetValue("IIN");
pspCardOutputDetails.GetValue("Last4");
pspCardOutputDetails.GetValue("NumberLength");
pspCardOutputDetails.GetValue("MaskedNumber");
pspCardOutputDetails.GetValue("MaskedNumberAlternative");


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

response.GetValue("psp_AlreadyUsed");
response.GetValue("psp_CreatedAt");
response.GetValue("psp_UpdatedAt");
