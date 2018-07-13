RootElement data = new RootElement();

data.add("Invoice", "54877555");
data.add("InvoiceDate", "2017-10-23");
data.add("InvoiceAmount", "15050");
data.add("InvoiceCurrency", "032");

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

data.add("Person", Person);

ComplexElement Address = new ComplexElement();
Address.add("AdditionalInfo", "2 A");
Address.add("City", "Miami");
Address.add("Country", "USA");
Address.add("HouseNumber", "1245");
Address.add("StateProvince", "Florida");
Address.add("Street", "Av. Collins");
Address.add("ZipCode", "33140");

data.add("Address", Address);
