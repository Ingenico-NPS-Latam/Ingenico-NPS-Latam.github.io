ComplexElement billingDetails = response.getComplexElement("BillingDetails");

fmt.Printf(billingDetails.Invoice)
fmt.Printf(billingDetails.InvoiceDate)
fmt.Printf(billingDetails.InvoiceAmount)
fmt.Printf(billingDetails.InvoiceCurrency)

person := billingDetails.Person
fmt.Printf(person.DateOfBirth)
fmt.Printf(person.FirstName)
fmt.Printf(person.Gender)
fmt.Printf(person.IDNumber)
fmt.Printf(person.IDType)
fmt.Printf(person.LastName)
fmt.Printf(person.MiddleName)
fmt.Printf(person.Nationality)
fmt.Printf(person.PhoneNumber1)
fmt.Printf(person.PhoneNumber2)


address := billingDetails.Address
fmt.Printf(address.AdditionalInfo)
fmt.Printf(address.City)
fmt.Printf(address.Country)
fmt.Printf(address.HouseNumber)
fmt.Printf(address.StateProvince)
fmt.Printf(address.Street)
fmt.Printf(address.ZipCode)

