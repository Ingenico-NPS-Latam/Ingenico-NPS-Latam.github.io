RootElement data = new RootElement();


ComplexElement pspPaymentMethodInputDetails = new ComplexElement();
pspPaymentMethodInputDetails.add("PaymentMethodToken", "KCVMXsbue5fUKOoAxvp1PTJ94gxv2dQM");
pspPaymentMethodInputDetails.add("PaymentMethodTag", "Corporate card");

ComplexElement CardInputDetails = new ComplexElement();
CardInputDetails.add("Number", "4507990000000010");
CardInputDetails.add("ExpirationDate", "2501");
CardInputDetails.add("SecurityCode", "123");
CardInputDetails.add("HolderName", "JOHN DOE");

pspPaymentMethodInputDetails.add("CardInputDetails", CardInputDetails);

ComplexElement Person = new ComplexElement();
Person.add("DateOfBirth", "1979-01-12");
Person.add("FirstName", "John");
Person.add("Gender", "M");
Person.add("IDNumber", "54111111");
Person.add("IDType", "200");
Person.add("LastName", "Doe");
Person.add("MiddleName", "Michael");
Person.add("Nationality", "ARG");
Person.add("PhoneNumber1", "+1 011 11111111");
Person.add("PhoneNumber2", "+1 011 22222222");

pspPaymentMethodInputDetails.add("Person", Person);

ComplexElement Address = new ComplexElement();
Address.add("AdditionalInfo", "2 A");
Address.add("City", "Miami");
Address.add("Country", "USA");
Address.add("HouseNumber", "1245");
Address.add("StateProvince", "Florida");
Address.add("Street", "Av. Collins");
Address.add("ZipCode", "33140");

pspPaymentMethodInputDetails.add("Address", Address);

data.add("psp_PaymentMethodInputDetails", pspPaymentMethodInputDetails);
