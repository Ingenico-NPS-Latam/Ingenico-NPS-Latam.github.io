using System;
using NpsSDK;

ComplexElement PaymentMethodsOutputDetails = response.GetComplexElement("PaymentMethodsOutputDetails");


ComplexElement pspPaymentMethodsOutputDetails = PaymentMethodsOutputDetails.GetComplexElement("psp_PaymentMethodsOutputDetails");
pspPaymentMethodsOutputDetails.GetValue("PaymentMethodId");
pspPaymentMethodsOutputDetails.GetValue("PaymentMethodTag");
pspPaymentMethodsOutputDetails.GetValue("Product");

ComplexElement cardOutputDetails = psp_PaymentMethodsOutputDetails.GetComplexElement("CardOutputDetails");
cardOutputDetails.GetValue("ExpirationDate");
cardOutputDetails.GetValue("ExpirationYear");
cardOutputDetails.GetValue("ExpirationMonth");
cardOutputDetails.GetValue("HolderName");
cardOutputDetails.GetValue("IIN");
cardOutputDetails.GetValue("Last4");
cardOutputDetails.GetValue("MaskedNumber");
cardOutputDetails.GetValue("MaskedNumberAlternative");

pspPaymentMethodsOutputDetails.GetValue("FingerPrint");

ComplexElement person = psp_PaymentMethodsOutputDetails.GetComplexElement("Person");
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


ComplexElement address = psp_PaymentMethodsOutputDetails.GetComplexElement("Address");
address.GetValue("AdditionalInfo");
address.GetValue("City");
address.GetValue("Country");
address.GetValue("HouseNumber");
address.GetValue("StateProvince");
address.GetValue("Street");
address.GetValue("ZipCode");

pspPaymentMethodsOutputDetails.GetValue("CreatedAt");
pspPaymentMethodsOutputDetails.GetValue("UpdatedAt");

