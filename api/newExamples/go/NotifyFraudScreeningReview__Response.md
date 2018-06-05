resp, err := service.NotifyFraudScreeningReview(notifyFraudScreeningReview)

fmt.Printf(resp.Psp_ResponseCod)
fmt.Printf(resp.Psp_ResponseMsg)
fmt.Printf(resp.Psp_ResponseExtended)
fmt.Printf(resp.Psp_MerchantId)
fmt.Printf(resp.Psp_PosDateTime)
