RootElement data = new RootElement();


ComplexElement pspPaymentMethodsOutputDetails = new ComplexElement();
pspPaymentMethodsOutputDetails.Add("PaymentMethodId", "Nzmd7DyGytXXC5PtKwnCsXXuQWHJB9EE");
pspPaymentMethodsOutputDetails.Add("PaymentMethodTag", "My Credit Card");
pspPaymentMethodsOutputDetails.Add("Product", "14");

ComplexElement CardOutputDetails = new ComplexElement();
CardOutputDetails.Add("ExpirationDate", "2501");
CardOutputDetails.Add("ExpirationYear", "2025");
CardOutputDetails.Add("ExpirationMonth", "01");
CardOutputDetails.Add("HolderName", "JOHN DOE");
CardOutputDetails.Add("IIN", "450799");
CardOutputDetails.Add("Last4", "0010");
CardOutputDetails.Add("MaskedNumber", "450799******0010");
CardOutputDetails.Add("MaskedNumberAlternative", "************0010");

pspPaymentMethodsOutputDetails.Add("CardOutputDetails", CardOutputDetails);
pspPaymentMethodsOutputDetails.Add("FingerPrint", "mGaXrr7u5sOONy68YuC55yJ0Q6xcByTIxzO1RPFcZbpEuClw");

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

pspPaymentMethodsOutputDetails.Add("Person", Person);

ComplexElement Address = new ComplexElement();
Address.Add("AdditionalInfo", "2 A");
Address.Add("City", "Miami");
Address.Add("Country", "USA");
Address.Add("HouseNumber", "1245");
Address.Add("StateProvince", "Florida");
Address.Add("Street", "Av. Collins");
Address.Add("ZipCode", "33140");

pspPaymentMethodsOutputDetails.Add("Address", Address);
pspPaymentMethodsOutputDetails.Add("CreatedAt", "2008-01-12 13:05:35-03:00");
pspPaymentMethodsOutputDetails.Add("UpdatedAt", "2008-01-12 13:06:35-03:00");

data.Add("psp_PaymentMethodsOutputDetails", pspPaymentMethodsOutputDetails);
