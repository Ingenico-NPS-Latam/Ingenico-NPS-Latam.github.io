response, err := service.CreatePaymentMethodToken(createPaymentMethodToken)

fmt.Printf(response.Psp_ResponseCod)
fmt.Printf(response.Psp_ResponseMsg)
fmt.Printf(response.Psp_MerchantId)
fmt.Printf(response.Psp_PaymentMethodToken)
fmt.Printf(response.Psp_Product)

pspWalletOutputDetails := response.Psp_WalletOutputDetails

cardOutputDetails := psp_WalletOutputDetails.CardOutputDetails
fmt.Printf(cardOutputDetails.ExpirationDate)
fmt.Printf(cardOutputDetails.ExpirationYear)
fmt.Printf(cardOutputDetails.ExpirationMonth)
fmt.Printf(cardOutputDetails.HolderName)
fmt.Printf(cardOutputDetails.IIN)
fmt.Printf(cardOutputDetails.Last4)
fmt.Printf(cardOutputDetails.NumberLength)
fmt.Printf(cardOutputDetails.MaskedNumber)
fmt.Printf(cardOutputDetails.MaskedNumberAlternative)

shippingDetails := psp_WalletOutputDetails.ShippingDetails
fmt.Printf(shippingDetails.Method)

primaryRecipient := ShippingDetails.PrimaryRecipient
fmt.Printf(primaryRecipient.FirstName)
fmt.Printf(primaryRecipient.PhoneNumber1)

address := ShippingDetails.Address
fmt.Printf(address.Street)
fmt.Printf(address.HouseNumber)
fmt.Printf(address.AdditionalInfo)
fmt.Printf(address.City)
fmt.Printf(address.Country)
fmt.Printf(address.ZipCode)

pspAddress := response.Psp_Address
fmt.Printf(pspAddress.Street)
fmt.Printf(pspAddress.AdditionalInfo)
fmt.Printf(pspAddress.City)
fmt.Printf(pspAddress.Country)
fmt.Printf(pspAddress.ZipCode)
fmt.Printf(response.Psp_AlreadyUsed)
fmt.Printf(response.Psp_CreatedAt)
fmt.Printf(response.Psp_UpdatedAt)
