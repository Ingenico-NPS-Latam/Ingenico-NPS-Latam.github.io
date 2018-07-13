PaymentsMethodOutputDetails := nps.NewPaymentsMethodOutputDetailsStruct()

pspPaymentMethodsOutputDetails := nps.NewPaymentMethodsOutputDetailsStruct()
pspPaymentMethodsOutputDetails.PaymentMethodId = "Nzmd7DyGytXXC5PtKwnCsXXuQWHJB9EE"
pspPaymentMethodsOutputDetails.PaymentMethodTag = "My Credit Card"
pspPaymentMethodsOutputDetails.Product = "14"

CardOutputDetails := nps.NewCardOutputDetailsStruct()
CardOutputDetails.ExpirationDate = "2501"
CardOutputDetails.ExpirationYear = "2025"
CardOutputDetails.ExpirationMonth = "01"
CardOutputDetails.HolderName = "JOHN DOE"
CardOutputDetails.IIN = "450799"
CardOutputDetails.Last4 = "0010"
CardOutputDetails.MaskedNumber = "450799******0010"
CardOutputDetails.MaskedNumberAlternative = "************0010"

pspPaymentMethodsOutputDetails.CardOutputDetails = CardOutputDetails
pspPaymentMethodsOutputDetails.FingerPrint = "mGaXrr7u5sOONy68YuC55yJ0Q6xcByTIxzO1RPFcZbpEuClw"

Person := nps.NewPersonStruct()
Person.DateOfBirth = "1979-01-12"
Person.FirstName = "John"
Person.Gender = "M"
Person.IDNumber = "54111111"
Person.IDType = "200"
Person.LastName = "Doe"
Person.MiddleName = "Michael"
Person.Nationality = "ARG"
Person.PhoneNumber1 = "+1 011 11111111"
Person.PhoneNumber2 = "+1 011 22222222"

pspPaymentMethodsOutputDetails.Person = Person

Address := nps.NewAddressStruct()
Address.AdditionalInfo = "2 A"
Address.City = "Miami"
Address.Country = "USA"
Address.HouseNumber = "1245"
Address.StateProvince = "Florida"
Address.Street = "Av. Collins"
Address.ZipCode = "33140"

pspPaymentMethodsOutputDetails.Address = Address
pspPaymentMethodsOutputDetails.CreatedAt = "2008-01-12 13:05:35-03:00"
pspPaymentMethodsOutputDetails.UpdatedAt = "2008-01-12 13:06:35-03:00"

PaymentsMethodOutputDetails.psp_PaymentMethodsOutputDetails = pspPaymentMethodsOutputDetails
