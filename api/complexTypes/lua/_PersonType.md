ComplexElement person = response.getComplexElement("Person");


local pspPerson = person.psp_Person
print(pspPerson.DateOfBirth)
print(pspPerson.FirstName)
print(pspPerson.Gender)
print(pspPerson.IDNumber)
print(pspPerson.IDType)
print(pspPerson.LastName)
print(pspPerson.MiddleName)
print(pspPerson.Nationality)
print(pspPerson.PhoneNumber1)
print(pspPerson.PhoneNumber2)

