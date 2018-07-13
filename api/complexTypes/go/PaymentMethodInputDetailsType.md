PaymentMethodInputDetails := nps.NewPaymentMethodInputDetailsStruct()

pspPaymentMethodInputDetails := nps.NewPaymentMethodInputDetailsStruct()
pspPaymentMethodInputDetails.PaymentMethodToken = "KCVMXsbue5fUKOoAxvp1PTJ94gxv2dQM"
pspPaymentMethodInputDetails.PaymentMethodTag = "Corporate card"

CardInputDetails := nps.NewCardInputDetailsStruct()
CardInputDetails.Number = "4507990000000010"
CardInputDetails.ExpirationDate = "2501"
CardInputDetails.SecurityCode = "123"
CardInputDetails.HolderName = "JOHN DOE"

pspPaymentMethodInputDetails.CardInputDetails = CardInputDetails

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

pspPaymentMethodInputDetails.Person = Person

Address := nps.NewAddressStruct()
Address.AdditionalInfo = "2 A"
Address.City = "Miami"
Address.Country = "USA"
Address.HouseNumber = "1245"
Address.StateProvince = "Florida"
Address.Street = "Av. Collins"
Address.ZipCode = "33140"

pspPaymentMethodInputDetails.Address = Address

PaymentMethodInputDetails.psp_PaymentMethodInputDetails = pspPaymentMethodInputDetails
