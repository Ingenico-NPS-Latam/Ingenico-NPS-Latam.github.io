response, err := service.SplitPayOnLine_3p(splitPayOnLine3p)

fmt.Printf(response.Psp_ResponseCod)
fmt.Printf(response.Psp_ResponseMsg)
fmt.Printf(response.Psp_TransactionId)
fmt.Printf(response.Psp_Session3p)
fmt.Printf(response.Psp_FrontPSP_URL)
fmt.Printf(response.Psp_MerchantId)
fmt.Printf(response.Psp_MerchTxRef)
fmt.Printf(response.Psp_MerchOrderId)
fmt.Printf(response.Psp_Amount)
fmt.Printf(response.Psp_Currency)
fmt.Printf(response.Psp_Country)
fmt.Printf(response.Psp_Product)
fmt.Printf(response.Psp_PosDateTime)

pspTransactions := response.Psp_Transactions

pspTransactions1 := pspTransactions.Items[1];
fmt.Printf(pspTransactions1.Psp_MerchantId)
fmt.Printf(pspTransactions1.Psp_TransactionId)
fmt.Printf(pspTransactions1.Psp_MerchTxRef)
fmt.Printf(pspTransactions1.Psp_Product)
fmt.Printf(pspTransactions1.Psp_Amount)
fmt.Printf(pspTransactions1.Psp_NumPayments)
fmt.Printf(pspTransactions1.Psp_CreatedAt)


pspTransactions2 := pspTransactions.Items[2];
fmt.Printf(pspTransactions2.Psp_MerchantId)
fmt.Printf(pspTransactions2.Psp_TransactionId)
fmt.Printf(pspTransactions2.Psp_MerchTxRef)
fmt.Printf(pspTransactions2.Psp_Product)
fmt.Printf(pspTransactions2.Psp_Amount)
fmt.Printf(pspTransactions2.Psp_NumPayments)
fmt.Printf(pspTransactions2.Psp_CreatedAt)


