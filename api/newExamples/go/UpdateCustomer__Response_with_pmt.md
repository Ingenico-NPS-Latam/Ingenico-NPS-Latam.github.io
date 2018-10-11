response, err := service.UpdateCustomer(updateCustomer)

fmt.Printf(response.Psp_ResponseCod)
fmt.Printf(response.Psp_ResponseMsg)
fmt.Printf(response.Psp_MerchantId)
fmt.Printf(response.Psp_CustomerId)
fmt.Printf(response.Psp_EmailAddress)
fmt.Printf(response.Psp_AlternativeEmailAddress)
fmt.Printf(response.Psp_AccountID)
fmt.Printf(response.Psp_AccountCreatedAt)
fmt.Printf(response.Psp_DefaultPaymentMethodId)

pspPaymentMethods := response.Psp_PaymentMethods

pspPaymentMethods1 := pspPaymentMethods.Items[1];
fmt.Printf(pspPaymentMethods1.PaymentMethodId)
fmt.Printf(pspPaymentMethods1.Product)

cardOutputDetails := pspPaymentMethods1.CardOutputDetails
fmt.Printf(cardOutputDetails.ExpirationDate)
fmt.Printf(cardOutputDetails.ExpirationYear)
fmt.Printf(cardOutputDetails.ExpirationMonth)
fmt.Printf(cardOutputDetails.HolderName)
fmt.Printf(cardOutputDetails.IIN)
fmt.Printf(cardOutputDetails.Last4)
fmt.Printf(cardOutputDetails.NumberLength)
fmt.Printf(cardOutputDetails.MaskedNumber)
fmt.Printf(cardOutputDetails.MaskedNumberAlternative)
fmt.Printf(pspPaymentMethods1.FingerPrint)

person := pspPaymentMethods1.Person
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

address := pspPaymentMethods1.Address
fmt.Printf(address.Street)
fmt.Printf(address.HouseNumber)
fmt.Printf(address.AdditionalInfo)
fmt.Printf(address.City)
fmt.Printf(address.StateProvince)
fmt.Printf(address.Country)
fmt.Printf(address.ZipCode)
fmt.Printf(pspPaymentMethods1.CreatedAt)
fmt.Printf(pspPaymentMethods1.UpdatedAt)

fmt.Printf(response.Psp_PosDateTime)
