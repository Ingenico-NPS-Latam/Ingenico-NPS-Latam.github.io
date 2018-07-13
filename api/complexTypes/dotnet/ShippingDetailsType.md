RootElement data = new RootElement();


ComplexElement ShippingDetails = new ComplexElement();
ShippingDetails.Add("TrackingNumber", "154DDD54DWW11");
ShippingDetails.Add("Method", "1");
ShippingDetails.Add("Carrier", "200");
ShippingDetails.Add("DeliveryDate", "2014-11-20");
ShippingDetails.Add("FreightAmount", "15000");
ShippingDetails.Add("GiftMessage", "Happy Birthday!");
ShippingDetails.Add("GiftWrapping", "1");

ComplexElement PrimaryRecipient = new ComplexElement();
PrimaryRecipient.Add("DateOfBirth", "1979-01-12");
PrimaryRecipient.Add("FirstName", "John");
PrimaryRecipient.Add("Gender", "M");
PrimaryRecipient.Add("IDNumber", "54111111");
PrimaryRecipient.Add("IDType", "200");
PrimaryRecipient.Add("LastName", "Doe");
PrimaryRecipient.Add("MiddleName", "Michael");
PrimaryRecipient.Add("Nationality", "ARG");
PrimaryRecipient.Add("PhoneNumber1", "+1 011 11111111");
PrimaryRecipient.Add("PhoneNumber2", "+1 011 22222222");

ShippingDetails.Add("PrimaryRecipient", PrimaryRecipient);

ComplexElement SecondaryRecipient = new ComplexElement();
SecondaryRecipient.Add("DateOfBirth", "1979-01-12");
SecondaryRecipient.Add("FirstName", "John");
SecondaryRecipient.Add("Gender", "M");
SecondaryRecipient.Add("IDNumber", "54111111");
SecondaryRecipient.Add("IDType", "200");
SecondaryRecipient.Add("LastName", "Doe");
SecondaryRecipient.Add("MiddleName", "Michael");
SecondaryRecipient.Add("Nationality", "ARG");
SecondaryRecipient.Add("PhoneNumber1", "+1 011 11111111");
SecondaryRecipient.Add("PhoneNumber2", "+1 011 22222222");

ShippingDetails.Add("SecondaryRecipient", SecondaryRecipient);

ComplexElement Address = new ComplexElement();
Address.Add("AdditionalInfo", "2 A");
Address.Add("City", "Miami");
Address.Add("Country", "USA");
Address.Add("HouseNumber", "1245");
Address.Add("StateProvince", "Florida");
Address.Add("Street", "Av. Collins");
Address.Add("ZipCode", "33140");

ShippingDetails.Add("Address", Address);

data.Add("ShippingDetails", ShippingDetails);
