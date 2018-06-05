ComplexElement paymentMethodsOutputDetails = response.getComplexElement("PaymentMethodsOutputDetails");


pspPaymentMethodsOutputDetails := paymentMethodsOutputDetails.Psp_PaymentMethodsOutputDetails
fmt.Printf(pspPaymentMethodsOutputDetails.PaymentMethodId)
fmt.Printf(pspPaymentMethodsOutputDetails.PaymentMethodTag)
fmt.Printf(pspPaymentMethodsOutputDetails.Product)

cardOutputDetails := psp_PaymentMethodsOutputDetails.CardOutputDetails
fmt.Printf(cardOutputDetails.ExpirationDate)
fmt.Printf(cardOutputDetails.ExpirationYear)
fmt.Printf(cardOutputDetails.ExpirationMonth)
fmt.Printf(cardOutputDetails.HolderName)
fmt.Printf(cardOutputDetails.IIN)
fmt.Printf(cardOutputDetails.Last4)
fmt.Printf(cardOutputDetails.MaskedNumber)
fmt.Printf(cardOutputDetails.MaskedNumberAlternative)

fmt.Printf(pspPaymentMethodsOutputDetails.FingerPrint)

person := psp_PaymentMethodsOutputDetails.Person
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


address := psp_PaymentMethodsOutputDetails.Address
fmt.Printf(address.AdditionalInfo)
fmt.Printf(address.City)
fmt.Printf(address.Country)
fmt.Printf(address.HouseNumber)
fmt.Printf(address.StateProvince)
fmt.Printf(address.Street)
fmt.Printf(address.ZipCode)

fmt.Printf(pspPaymentMethodsOutputDetails.CreatedAt)
fmt.Printf(pspPaymentMethodsOutputDetails.UpdatedAt)

