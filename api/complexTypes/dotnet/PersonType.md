RootElement data = new RootElement();


ComplexElement pspPerson = new ComplexElement();
pspPerson.Add("DateOfBirth", "1979-01-12");
pspPerson.Add("FirstName", "John");
pspPerson.Add("Gender", "M");
pspPerson.Add("IDNumber", "54111111");
pspPerson.Add("IDType", "200");
pspPerson.Add("LastName", "Doe");
pspPerson.Add("MiddleName", "Michael");
pspPerson.Add("Nationality", "ARG");
pspPerson.Add("PhoneNumber1", "+1 011 11111111");
pspPerson.Add("PhoneNumber2", "+1 011 22222222");

data.Add("psp_Person", pspPerson);
