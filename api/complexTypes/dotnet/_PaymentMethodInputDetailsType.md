using System;
using NpsSDK;

ComplexElement PaymentMethodInputDetails = response.GetComplexElement("PaymentMethodInputDetails");


ComplexElement pspPaymentMethodInputDetails = PaymentMethodInputDetails.GetComplexElement("psp_PaymentMethodInputDetails");
pspPaymentMethodInputDetails.GetValue("PaymentMethodToken");
pspPaymentMethodInputDetails.GetValue("PaymentMethodTag");

ComplexElement cardInputDetails = psp_PaymentMethodInputDetails.GetComplexElement("CardInputDetails");
cardInputDetails.GetValue("Number");
cardInputDetails.GetValue("ExpirationDate");
cardInputDetails.GetValue("SecurityCode");
cardInputDetails.GetValue("HolderName");


ComplexElement person = psp_PaymentMethodInputDetails.GetComplexElement("Person");
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


ComplexElement address = psp_PaymentMethodInputDetails.GetComplexElement("Address");
address.GetValue("AdditionalInfo");
address.GetValue("City");
address.GetValue("Country");
address.GetValue("HouseNumber");
address.GetValue("StateProvince");
address.GetValue("Street");
address.GetValue("ZipCode");


