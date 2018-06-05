response, err := service.QueryCardNumber(queryCardNumber)

fmt.Printf(response.Psp_ResponseCod)
fmt.Printf(response.Psp_ResponseMsg)
fmt.Printf(response.Psp_MerchantId)
fmt.Printf(response.Psp_QueryCriteria)
fmt.Printf(response.Psp_QueryCriteriaId)
fmt.Printf(response.Psp_PosDateTime)
fmt.Printf(response.Psp_CardNumber)
