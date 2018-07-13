RootElement data = new RootElement();

data.Add("Invoice", "54877555");
data.Add("InvoiceDate", "2017-10-23");
data.Add("InvoiceAmount", "15050");
data.Add("InvoiceCurrency", "032");

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

data.Add("Person", Person);

ComplexElement Address = new ComplexElement();
Address.Add("AdditionalInfo", "2 A");
Address.Add("City", "Miami");
Address.Add("Country", "USA");
Address.Add("HouseNumber", "1245");
Address.Add("StateProvince", "Florida");
Address.Add("Street", "Av. Collins");
Address.Add("ZipCode", "33140");

data.Add("Address", Address);
