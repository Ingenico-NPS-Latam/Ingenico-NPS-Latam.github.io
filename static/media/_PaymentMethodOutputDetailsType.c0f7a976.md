using System;
using NpsSDK;

ComplexElement PaymentMethodOutputDetails = response.GetComplexElement("PaymentMethodOutputDetails");


ComplexElement pspPaymentMethodOutputDetails = PaymentMethodOutputDetails.GetComplexElement("psp_PaymentMethodOutputDetails");
pspPaymentMethodOutputDetails.GetValue("PaymentMethodId");
pspPaymentMethodOutputDetails.GetValue("PaymentMethodTag");
pspPaymentMethodOutputDetails.GetValue("Product");

ComplexElement cardOutputDetails = psp_PaymentMethodOutputDetails.GetComplexElement("CardOutputDetails");
cardOutputDetails.GetValue("ExpirationDate");
cardOutputDetails.GetValue("ExpirationYear");
cardOutputDetails.GetValue("ExpirationMonth");
cardOutputDetails.GetValue("HolderName");
cardOutputDetails.GetValue("IIN");
cardOutputDetails.GetValue("Last4");
cardOutputDetails.GetValue("NumberLength");
cardOutputDetails.GetValue("MaskedNumber");
cardOutputDetails.GetValue("MaskedNumberAlternative");

pspPaymentMethodOutputDetails.GetValue("FingerPrint");

ComplexElement person = psp_PaymentMethodOutputDetails.GetComplexElement("Person");
person.GetValue("DateOfBirth");
person.GetValue("FirstName");
person.GetValue("Gender");
person.GetValue("IDNumber");
person.GetValue("IDType");
person.GetValue("LastName");
person.GetValue("MiddleName");
person.GetValue("Nationality");
person.GetValue("PhoneNumber1");
person.GetValue("PhoneNumber2");


ComplexElement address = psp_PaymentMethodOutputDetails.GetComplexElement("Address");
address.GetValue("AdditionalInfo");
address.GetValue("City");
address.GetValue("Country");
address.GetValue("HouseNumber");
address.GetValue("StateProvince");
address.GetValue("Street");
address.GetValue("ZipCode");

pspPaymentMethodOutputDetails.GetValue("CreatedAt");
pspPaymentMethodOutputDetails.GetValue("UpdatedAt");

