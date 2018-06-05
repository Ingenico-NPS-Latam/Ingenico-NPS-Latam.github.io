ComplexElement paymentMethodOutputDetails = response.getComplexElement("PaymentMethodOutputDetails");


pspPaymentMethodOutputDetails := paymentMethodOutputDetails.Psp_PaymentMethodOutputDetails
fmt.Printf(pspPaymentMethodOutputDetails.PaymentMethodId)
fmt.Printf(pspPaymentMethodOutputDetails.PaymentMethodTag)
fmt.Printf(pspPaymentMethodOutputDetails.Product)

cardOutputDetails := psp_PaymentMethodOutputDetails.CardOutputDetails
fmt.Printf(cardOutputDetails.ExpirationDate)
fmt.Printf(cardOutputDetails.ExpirationYear)
fmt.Printf(cardOutputDetails.ExpirationMonth)
fmt.Printf(cardOutputDetails.HolderName)
fmt.Printf(cardOutputDetails.IIN)
fmt.Printf(cardOutputDetails.Last4)
fmt.Printf(cardOutputDetails.NumberLength)
fmt.Printf(cardOutputDetails.MaskedNumber)
fmt.Printf(cardOutputDetails.MaskedNumberAlternative)

fmt.Printf(pspPaymentMethodOutputDetails.FingerPrint)

person := psp_PaymentMethodOutputDetails.Person
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


address := psp_PaymentMethodOutputDetails.Address
fmt.Printf(address.AdditionalInfo)
fmt.Printf(address.City)
fmt.Printf(address.Country)
fmt.Printf(address.HouseNumber)
fmt.Printf(address.StateProvince)
fmt.Printf(address.Street)
fmt.Printf(address.ZipCode)

fmt.Printf(pspPaymentMethodOutputDetails.CreatedAt)
fmt.Printf(pspPaymentMethodOutputDetails.UpdatedAt)

