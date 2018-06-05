response, err := service.GetIINDetails(getIINDetails)

fmt.Printf(response.Psp_ResponseCod)
fmt.Printf(response.Psp_ResponseMsg)
fmt.Printf(response.Psp_MerchantId)
fmt.Printf(response.Psp_Product)
fmt.Printf(response.Psp_PosDateTime)
