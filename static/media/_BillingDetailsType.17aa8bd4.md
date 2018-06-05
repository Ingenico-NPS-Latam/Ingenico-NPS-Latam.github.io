ComplexElement billingDetails = response.getComplexElement("BillingDetails");

print(billingDetails.Invoice)
print(billingDetails.InvoiceDate)
print(billingDetails.InvoiceAmount)
print(billingDetails.InvoiceCurrency)

local person = billingDetails.Person
print(person.DateOfBirth)
print(person.FirstName)
print(person.Gender)
print(person.IDNumber)
print(person.IDType)
print(person.LastName)
print(person.MiddleName)
print(person.Nationality)
print(person.PhoneNumber1)
print(person.PhoneNumber2)


local address = billingDetails.Address
print(address.AdditionalInfo)
print(address.City)
print(address.Country)
print(address.HouseNumber)
print(address.StateProvince)
print(address.Street)
print(address.ZipCode)

