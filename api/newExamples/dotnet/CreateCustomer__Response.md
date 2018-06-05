using System;
using NpsSDK;

RootElement response = npsSdk.CreateCustomer(data);

response.GetValue("psp_ResponseCod");
response.GetValue("psp_ResponseMsg");
response.GetValue("psp_MerchantId");
response.GetValue("psp_CustomerId");
response.GetValue("psp_EmailAddress");
response.GetValue("psp_AlternativeEmailAddress");
response.GetValue("psp_AccountID");
response.GetValue("psp_AccountCreatedAt");
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

ComplexElement person = pspPaymentMethods1.GetComplexElement("Person");
person.GetValue("FirstName");
person.GetValue("LastName");
person.GetValue("MiddleName");
person.GetValue("PhoneNumber1");
person.GetValue("PhoneNumber2");
person.GetValue("Gender");
person.GetValue("DateOfBirth");
person.GetValue("Nationality");
person.GetValue("IDNumber");
person.GetValue("IDType");


ComplexElement address = pspPaymentMethods1.GetComplexElement("Address");
address.GetValue("Street");
address.GetValue("HouseNumber");
address.GetValue("AdditionalInfo");
address.GetValue("City");
address.GetValue("StateProvince");
address.GetValue("Country");
address.GetValue("ZipCode");

pspPaymentMethods1.GetValue("CreatedAt");
pspPaymentMethods1.GetValue("UpdatedAt");


response.GetValue("psp_PosDateTime");
