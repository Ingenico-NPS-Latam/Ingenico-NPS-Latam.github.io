using System;
using NpsSDK;

RootElement response = npsSdk.DeletePaymentMethod(data);

response.GetValue("psp_ResponseCod");
response.GetValue("psp_ResponseMsg");
response.GetValue("psp_MerchantId");

ComplexElement pspPaymentMethod = response.GetComplexElement("psp_PaymentMethod");
pspPaymentMethod.GetValue("PaymentMethodId");
pspPaymentMethod.GetValue("PaymentMethodTag");
pspPaymentMethod.GetValue("Product");

ComplexElement cardOutputDetails = psp_PaymentMethod.GetComplexElement("CardOutputDetails");
cardOutputDetails.GetValue("ExpirationDate");
cardOutputDetails.GetValue("ExpirationYear");
cardOutputDetails.GetValue("ExpirationMonth");
cardOutputDetails.GetValue("HolderName");
cardOutputDetails.GetValue("IIN");
cardOutputDetails.GetValue("Last4");
cardOutputDetails.GetValue("NumberLength");
cardOutputDetails.GetValue("MaskedNumber");
cardOutputDetails.GetValue("MaskedNumberAlternative");

pspPaymentMethod.GetValue("FingerPrint");

ComplexElement person = psp_PaymentMethod.GetComplexElement("Person");
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


ComplexElement address = psp_PaymentMethod.GetComplexElement("Address");
address.GetValue("Street");
address.GetValue("HouseNumber");
address.GetValue("AdditionalInfo");
address.GetValue("City");
address.GetValue("StateProvince");
address.GetValue("Country");
address.GetValue("ZipCode");

pspPaymentMethod.GetValue("CreatedAt");
pspPaymentMethod.GetValue("UpdatedAt");

response.GetValue("psp_PosDateTime");
