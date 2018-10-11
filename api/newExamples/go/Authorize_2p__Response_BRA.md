response, err := service.Authorize_2p(authorize2p)

fmt.Printf(response.Psp_ResponseCod)
fmt.Printf(response.Psp_ResponseMsg)
fmt.Printf(response.Psp_ResponseExtended)
fmt.Printf(response.Psp_TransactionId)
fmt.Printf(response.Psp_MerchantId)
fmt.Printf(response.Psp_MerchTxRef)
fmt.Printf(response.Psp_MerchOrderId)
fmt.Printf(response.Psp_Amount)
fmt.Printf(response.Psp_NumPayments)
fmt.Printf(response.Psp_Currency)
fmt.Printf(response.Psp_Country)
fmt.Printf(response.Psp_Product)
fmt.Printf(response.Psp_CardNumber)
fmt.Printf(response.Psp_CardExpDate)
fmt.Printf(response.Psp_AuthorizationCode)
fmt.Printf(response.Psp_SequenceNumber)
fmt.Printf(response.Psp_ClTrnId)
fmt.Printf(response.Psp_ClExternalMerchant)
fmt.Printf(response.Psp_ClResponseCod)
fmt.Printf(response.Psp_ClResponseMsg)
fmt.Printf(response.Psp_PosDateTime)
fmt.Printf(response.Psp_Plan)
fmt.Printf(response.Psp_CreatedAt)

pspAmountAdditionalDetails := response.Psp_AmountAdditionalDetails
fmt.Printf(pspAmountAdditionalDetails.Tip)
fmt.Printf(pspAmountAdditionalDetails.Discount)

taxes := psp_AmountAdditionalDetails.Taxes

taxes1 := taxes.Items[1];
fmt.Printf(taxes1.TypeId)
fmt.Printf(taxes1.TypeDescription)
fmt.Printf(taxes1.Amount)
fmt.Printf(taxes1.Rate)
fmt.Printf(taxes1.BaseAmount)
fmt.Printf(taxes1.AppliedAmount)
fmt.Printf(taxes1.Remarks)


pspFraudScreeningResult := response.Psp_FraudScreeningResult
fmt.Printf(pspFraudScreeningResult.ResultCode)
fmt.Printf(pspFraudScreeningResult.ResultDescription)

pspVerificationServicesResult := response.Psp_VerificationServicesResult
fmt.Printf(pspVerificationServicesResult.ResultCodeCardSecurityCode)
fmt.Printf(pspVerificationServicesResult.ResultCodeBillingAddress)
fmt.Printf(pspVerificationServicesResult.ResultCodeBillingAddressZipCode)
fmt.Printf(pspVerificationServicesResult.ResultCodeBillingPersonIDType)
fmt.Printf(pspVerificationServicesResult.ResultCodeBillingPersonIDNumber)
fmt.Printf(pspVerificationServicesResult.ResultCodeBillingPersonDateOfBirth)
fmt.Printf(pspVerificationServicesResult.ResultCodeBillingPersonName)
fmt.Printf(pspVerificationServicesResult.ResultCodeBillingPersonPhoneNumber1)
fmt.Printf(pspVerificationServicesResult.ResultCodeCustomerEmailAddress)
