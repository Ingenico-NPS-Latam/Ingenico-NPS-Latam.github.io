response, err := service.CreateClientSession(createClientSession)

fmt.Printf(response.Psp_ResponseCod)
fmt.Printf(response.Psp_ResponseMsg)
fmt.Printf(response.Psp_MerchantId)
fmt.Printf(response.Psp_ClientSession)
fmt.Printf(response.Psp_PosDateTime)
fmt.Printf(response.Psp_CreatedAt)
