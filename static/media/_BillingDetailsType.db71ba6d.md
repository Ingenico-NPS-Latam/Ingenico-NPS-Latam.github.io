using System;
using NpsSDK;

ComplexElement BillingDetails = response.GetComplexElement("BillingDetails");

billingDetails.GetValue("Invoice");
billingDetails.GetValue("InvoiceDate");
billingDetails.GetValue("InvoiceAmount");
billingDetails.GetValue("InvoiceCurrency");

ComplexElement person = BillingDetails.GetComplexElement("Person");
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


ComplexElement address = BillingDetails.GetComplexElement("Address");
address.GetValue("AdditionalInfo");
address.GetValue("City");
address.GetValue("Country");
address.GetValue("HouseNumber");
address.GetValue("StateProvince");
address.GetValue("Street");
address.GetValue("ZipCode");

