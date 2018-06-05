using System;
using NpsSDK;

ComplexElement Person = response.GetComplexElement("Person");


ComplexElement pspPerson = Person.GetComplexElement("psp_Person");
pspPerson.GetValue("DateOfBirth");
pspPerson.GetValue("FirstName");
pspPerson.GetValue("Gender");
pspPerson.GetValue("IDNumber");
pspPerson.GetValue("IDType");
pspPerson.GetValue("LastName");
pspPerson.GetValue("MiddleName");
pspPerson.GetValue("Nationality");
pspPerson.GetValue("PhoneNumber1");
pspPerson.GetValue("PhoneNumber2");

