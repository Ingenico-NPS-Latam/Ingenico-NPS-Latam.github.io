response, err := service.NotifyFraudScreeningReview(notifyFraudScreeningReview)

fmt.Printf(response.Psp_ResponseCod)
fmt.Printf(response.Psp_ResponseMsg)
fmt.Printf(response.Psp_MerchantId)
fmt.Printf(response.Psp_Criteria)
fmt.Printf(response.Psp_CriteriaId)
fmt.Printf(response.Psp_PosDateTime)
