using System;
using NpsSDK;

ComplexElement ShippingDetails = response.GetComplexElement("ShippingDetails");


ComplexElement shippingDetails = ShippingDetails.GetComplexElement("ShippingDetails");
shippingDetails.GetValue("TrackingNumber");
shippingDetails.GetValue("Method");
shippingDetails.GetValue("Carrier");
shippingDetails.GetValue("DeliveryDate");
shippingDetails.GetValue("FreightAmount");
shippingDetails.GetValue("GiftMessage");
shippingDetails.GetValue("GiftWrapping");

ComplexElement primaryRecipient = ShippingDetails.GetComplexElement("PrimaryRecipient");
primaryRecipient.GetValue("DateOfBirth");
primaryRecipient.GetValue("FirstName");
primaryRecipient.GetValue("Gender");
primaryRecipient.GetValue("IDNumber");
primaryRecipient.GetValue("IDType");
primaryRecipient.GetValue("LastName");
primaryRecipient.GetValue("MiddleName");
primaryRecipient.GetValue("Nationality");
primaryRecipient.GetValue("PhoneNumber1");
primaryRecipient.GetValue("PhoneNumber2");


ComplexElement secondaryRecipient = ShippingDetails.GetComplexElement("SecondaryRecipient");
secondaryRecipient.GetValue("DateOfBirth");
secondaryRecipient.GetValue("FirstName");
secondaryRecipient.GetValue("Gender");
secondaryRecipient.GetValue("IDNumber");
secondaryRecipient.GetValue("IDType");
secondaryRecipient.GetValue("LastName");
secondaryRecipient.GetValue("MiddleName");
secondaryRecipient.GetValue("Nationality");
secondaryRecipient.GetValue("PhoneNumber1");
secondaryRecipient.GetValue("PhoneNumber2");


ComplexElement address = ShippingDetails.GetComplexElement("Address");
address.GetValue("AdditionalInfo");
address.GetValue("City");
address.GetValue("Country");
address.GetValue("HouseNumber");
address.GetValue("StateProvince");
address.GetValue("Street");
address.GetValue("ZipCode");


