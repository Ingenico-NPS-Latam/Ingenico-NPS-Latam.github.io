response, err := service.CreatePaymentMethodFromPayment(createPaymentMethodFromPayment)

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
fmt.Printf(cardOutputDetails.IIN)
fmt.Printf(cardOutputDetails.Last4)
fmt.Printf(cardOutputDetails.NumberLength)
fmt.Printf(cardOutputDetails.MaskedNumber)
fmt.Printf(cardOutputDetails.MaskedNumberAlternative)
fmt.Printf(pspPaymentMethod.FingerPrint)
fmt.Printf(pspPaymentMethod.CreatedAt)
fmt.Printf(pspPaymentMethod.UpdatedAt)
fmt.Printf(response.Psp_PosDateTime)
