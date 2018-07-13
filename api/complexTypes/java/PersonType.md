RootElement data = new RootElement();


ComplexElement pspPerson = new ComplexElement();
pspPerson.add("DateOfBirth", "1979-01-12");
pspPerson.add("FirstName", "John");
pspPerson.add("Gender", "M");
pspPerson.add("IDNumber", "54111111");
pspPerson.add("IDType", "200");
pspPerson.add("LastName", "Doe");
pspPerson.add("MiddleName", "Michael");
pspPerson.add("Nationality", "ARG");
pspPerson.add("PhoneNumber1", "+1 011 11111111");
pspPerson.add("PhoneNumber2", "+1 011 22222222");

data.add("psp_Person", pspPerson);
