response, err := service.CreatePaymentMethod(createPaymentMethod)

fmt.Printf(response.Psp_ResponseCod)
fmt.Printf(response.Psp_ResponseMsg)
fmt.Printf(response.Psp_MerchantId)

pspPaymentMethod := response.Psp_PaymentMethod
fmt.Printf(pspPaymentMethod.PaymentMethodId)
fmt.Printf(pspPaymentMethod.PaymentMethodTag)
fmt.Printf(pspPaymentMethod.Product)

cardOutputDetails := psp_PaymentMethod.CardOutputDetails
fmt.Printf(cardOutputDetails.ExpirationDate)
fmt.Printf(cardOutputDetails.ExpirationYear)
fmt.Printf(cardOutputDetails.ExpirationMonth)
fmt.Printf(cardOutputDetails.HolderName)
fmt.Printf(cardOutputDetails.IIN)
fmt.Printf(cardOutputDetails.Last4)
fmt.Printf(cardOutputDetails.NumberLength)
fmt.Printf(cardOutputDetails.MaskedNumber)
fmt.Printf(cardOutputDetails.MaskedNumberAlternative)
fmt.Printf(pspPaymentMethod.FingerPrint)

person := psp_PaymentMethod.Person
fmt.Printf(person.FirstName)
fmt.Printf(person.LastName)
fmt.Printf(person.MiddleName)
fmt.Printf(person.PhoneNumber1)
fmt.Printf(person.PhoneNumber2)
fmt.Printf(person.Gender)
fmt.Printf(person.DateOfBirth)
fmt.Printf(person.Nationality)
fmt.Printf(person.IDNumber)
fmt.Printf(person.IDType)

address := psp_PaymentMethod.Address
fmt.Printf(address.Street)
fmt.Printf(address.HouseNumber)
fmt.Printf(address.AdditionalInfo)
fmt.Printf(address.City)
fmt.Printf(address.StateProvince)
fmt.Printf(address.Country)
fmt.Printf(address.ZipCode)
fmt.Printf(pspPaymentMethod.CreatedAt)
fmt.Printf(pspPaymentMethod.UpdatedAt)
fmt.Printf(response.Psp_CustomerId)
fmt.Printf(response.Psp_PosDateTime)
