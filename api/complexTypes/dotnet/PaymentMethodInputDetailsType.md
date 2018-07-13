RootElement data = new RootElement();


ComplexElement pspPaymentMethodInputDetails = new ComplexElement();
pspPaymentMethodInputDetails.Add("PaymentMethodToken", "KCVMXsbue5fUKOoAxvp1PTJ94gxv2dQM");
pspPaymentMethodInputDetails.Add("PaymentMethodTag", "Corporate card");

ComplexElement CardInputDetails = new ComplexElement();
CardInputDetails.Add("Number", "4507990000000010");
CardInputDetails.Add("ExpirationDate", "2501");
CardInputDetails.Add("SecurityCode", "123");
CardInputDetails.Add("HolderName", "JOHN DOE");

pspPaymentMethodInputDetails.Add("CardInputDetails", CardInputDetails);

ComplexElement Person = new ComplexElement();
Person.Add("DateOfBirth", "1979-01-12");
Person.Add("FirstName", "John");
Person.Add("Gender", "M");
Person.Add("IDNumber", "54111111");
Person.Add("IDType", "200");
Person.Add("LastName", "Doe");
Person.Add("MiddleName", "Michael");
Person.Add("Nationality", "ARG");
Person.Add("PhoneNumber1", "+1 011 11111111");
Person.Add("PhoneNumber2", "+1 011 22222222");

pspPaymentMethodInputDetails.Add("Person", Person);

ComplexElement Address = new ComplexElement();
Address.Add("AdditionalInfo", "2 A");
Address.Add("City", "Miami");
Address.Add("Country", "USA");
Address.Add("HouseNumber", "1245");
Address.Add("StateProvince", "Florida");
Address.Add("Street", "Av. Collins");
Address.Add("ZipCode", "33140");

pspPaymentMethodInputDetails.Add("Address", Address);

data.Add("psp_PaymentMethodInputDetails", pspPaymentMethodInputDetails);
