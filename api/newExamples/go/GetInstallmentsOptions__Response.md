response, err := service.GetInstallmentsOptions(getInstallmentsOptions)

fmt.Printf(response.Psp_ResponseCod)
fmt.Printf(response.Psp_ResponseMsg)
fmt.Printf(response.Psp_MerchantId)
fmt.Printf(response.Psp_Amount)
fmt.Printf(response.Psp_Product)
fmt.Printf(response.Psp_Currency)
fmt.Printf(response.Psp_Country)
fmt.Printf(response.Psp_NumPayments)

pspInstallmentsOptions := response.Psp_InstallmentsOptions

pspInstallmentsOptions1 := pspInstallmentsOptions.Items[1];
fmt.Printf(pspInstallmentsOptions1.NumPayments)
fmt.Printf(pspInstallmentsOptions1.InstallmentAmount)

fmt.Printf(response.Psp_PosDateTime)
