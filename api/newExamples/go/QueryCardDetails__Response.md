resp, err := service.QueryCardDetails(queryCardDetails)

fmt.Printf(resp.Psp_ResponseCod)
fmt.Printf(resp.Psp_ResponseMsg)
fmt.Printf(resp.Psp_MerchantId)
fmt.Printf(resp.Psp_QueryCriteria)
fmt.Printf(resp.Psp_QueryCriteriaId)
fmt.Printf(resp.Psp_PosDateTime)

pspCardOutputDetails := resp.Psp_CardOutputDetails
fmt.Printf(pspCardOutputDetails.Number)
fmt.Printf(pspCardOutputDetails.ExpirationDate)
fmt.Printf(pspCardOutputDetails.ExpirationYear)
fmt.Printf(pspCardOutputDetails.ExpirationMonth)
fmt.Printf(pspCardOutputDetails.HolderName)
fmt.Printf(pspCardOutputDetails.IIN)
fmt.Printf(pspCardOutputDetails.Last4)
fmt.Printf(pspCardOutputDetails.NumberLength)
fmt.Printf(pspCardOutputDetails.MaskedNumber)
fmt.Printf(pspCardOutputDetails.MaskedNumberAlternative)

