ComplexElement person = response.getComplexElement("Person");


pspPerson := person.Psp_Person
fmt.Printf(pspPerson.DateOfBirth)
fmt.Printf(pspPerson.FirstName)
fmt.Printf(pspPerson.Gender)
fmt.Printf(pspPerson.IDNumber)
fmt.Printf(pspPerson.IDType)
fmt.Printf(pspPerson.LastName)
fmt.Printf(pspPerson.MiddleName)
fmt.Printf(pspPerson.Nationality)
fmt.Printf(pspPerson.PhoneNumber1)
fmt.Printf(pspPerson.PhoneNumber2)

