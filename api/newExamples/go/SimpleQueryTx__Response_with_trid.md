response, err := service.SimpleQueryTx(simpleQueryTx)

fmt.Printf(response.Psp_ResponseCod)
fmt.Printf(response.Psp_ResponseMsg)
fmt.Printf(response.Psp_MerchantId)
fmt.Printf(response.Psp_QueryCriteria)
fmt.Printf(response.Psp_QueryCriteriaId)
fmt.Printf(response.Psp_PosDateTime)

pspTransaction := response.Psp_Transaction
fmt.Printf(pspTransaction.Psp_ResponseCod)
fmt.Printf(pspTransaction.Psp_ResponseMsg)
fmt.Printf(pspTransaction.Psp_ResponseExtended)
fmt.Printf(pspTransaction.Psp_TransactionId)
fmt.Printf(pspTransaction.Psp_MerchantId)
fmt.Printf(pspTransaction.Psp_TxSource)
fmt.Printf(pspTransaction.Psp_Operation)
fmt.Printf(pspTransaction.Psp_MerchTxRef)
fmt.Printf(pspTransaction.Psp_MerchOrderId)
fmt.Printf(pspTransaction.Psp_Amount)
fmt.Printf(pspTransaction.Psp_NumPayments)
fmt.Printf(pspTransaction.Psp_Currency)
fmt.Printf(pspTransaction.Psp_Country)
fmt.Printf(pspTransaction.Psp_Product)
fmt.Printf(pspTransaction.Psp_AuthorizationCode)
fmt.Printf(pspTransaction.Psp_BatchNro)
fmt.Printf(pspTransaction.Psp_TicketNumber)
fmt.Printf(pspTransaction.Psp_CardNumber_FSD)
fmt.Printf(pspTransaction.Psp_CardNumber_LFD)
fmt.Printf(pspTransaction.Psp_CardMask)
fmt.Printf(pspTransaction.Psp_ClExternalMerchant)
fmt.Printf(pspTransaction.Psp_ClExternalTerminal)
fmt.Printf(pspTransaction.Psp_ClResponseCod)
fmt.Printf(pspTransaction.Psp_ClResponseMsg)
fmt.Printf(pspTransaction.Psp_PosDateTime)
fmt.Printf(pspTransaction.Psp_CreatedAt)

pspFraudScreeningResult := psp_Transaction.Psp_FraudScreeningResult
fmt.Printf(pspFraudScreeningResult.ResultCode)
fmt.Printf(pspFraudScreeningResult.ResultDescription)

pspVerificationServicesResult := psp_Transaction.Psp_VerificationServicesResult
fmt.Printf(pspVerificationServicesResult.ResultCodeCardSecurityCode)
fmt.Printf(pspVerificationServicesResult.ResultCodeBillingAddress)
fmt.Printf(pspVerificationServicesResult.ResultCodeBillingAddressZipCode)
fmt.Printf(pspVerificationServicesResult.ResultCodeBillingPersonIDType)
fmt.Printf(pspVerificationServicesResult.ResultCodeBillingPersonIDNumber)
fmt.Printf(pspVerificationServicesResult.ResultCodeBillingPersonDateOfBirth)
fmt.Printf(pspVerificationServicesResult.ResultCodeBillingPersonName)
fmt.Printf(pspVerificationServicesResult.ResultCodeBillingPersonPhoneNumber1)
fmt.Printf(pspVerificationServicesResult.ResultCodeCustomerEmailAddress)
