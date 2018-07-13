RootElement data = new RootElement();


ComplexElement pspPaymentMethodsOutputDetails = new ComplexElement();
pspPaymentMethodsOutputDetails.add("PaymentMethodId", "Nzmd7DyGytXXC5PtKwnCsXXuQWHJB9EE");
pspPaymentMethodsOutputDetails.add("PaymentMethodTag", "My Credit Card");
pspPaymentMethodsOutputDetails.add("Product", "14");

ComplexElement CardOutputDetails = new ComplexElement();
CardOutputDetails.add("ExpirationDate", "2501");
CardOutputDetails.add("ExpirationYear", "2025");
CardOutputDetails.add("ExpirationMonth", "01");
CardOutputDetails.add("HolderName", "JOHN DOE");
CardOutputDetails.add("IIN", "450799");
CardOutputDetails.add("Last4", "0010");
CardOutputDetails.add("MaskedNumber", "450799******0010");
CardOutputDetails.add("MaskedNumberAlternative", "************0010");

pspPaymentMethodsOutputDetails.add("CardOutputDetails", CardOutputDetails);
pspPaymentMethodsOutputDetails.add("FingerPrint", "mGaXrr7u5sOONy68YuC55yJ0Q6xcByTIxzO1RPFcZbpEuClw");

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

pspPaymentMethodsOutputDetails.add("Person", Person);

ComplexElement Address = new ComplexElement();
Address.add("AdditionalInfo", "2 A");
Address.add("City", "Miami");
Address.add("Country", "USA");
Address.add("HouseNumber", "1245");
Address.add("StateProvince", "Florida");
Address.add("Street", "Av. Collins");
Address.add("ZipCode", "33140");

pspPaymentMethodsOutputDetails.add("Address", Address);
pspPaymentMethodsOutputDetails.add("CreatedAt", "2008-01-12 13:05:35-03:00");
pspPaymentMethodsOutputDetails.add("UpdatedAt", "2008-01-12 13:06:35-03:00");

data.add("psp_PaymentMethodsOutputDetails", pspPaymentMethodsOutputDetails);
