ComplexElement paymentMethodInputDetails = response.getComplexElement("PaymentMethodInputDetails");


pspPaymentMethodInputDetails := paymentMethodInputDetails.Psp_PaymentMethodInputDetails
fmt.Printf(pspPaymentMethodInputDetails.PaymentMethodToken)
fmt.Printf(pspPaymentMethodInputDetails.PaymentMethodTag)

cardInputDetails := psp_PaymentMethodInputDetails.CardInputDetails
fmt.Printf(cardInputDetails.Number)
fmt.Printf(cardInputDetails.ExpirationDate)
fmt.Printf(cardInputDetails.SecurityCode)
fmt.Printf(cardInputDetails.HolderName)


person := psp_PaymentMethodInputDetails.Person
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


address := psp_PaymentMethodInputDetails.Address
fmt.Printf(address.AdditionalInfo)
fmt.Printf(address.City)
fmt.Printf(address.Country)
fmt.Printf(address.HouseNumber)
fmt.Printf(address.StateProvince)
fmt.Printf(address.Street)
fmt.Printf(address.ZipCode)


