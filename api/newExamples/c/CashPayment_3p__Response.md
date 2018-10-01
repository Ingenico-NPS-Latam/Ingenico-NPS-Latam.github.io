CASH_PAYMENT_3P_RESP_STRUCT Response, *pResponse;
pResponse = &Response;

printf("psp_ResponseCod: %s\n", pResponse->psp_ResponseCod);
printf("psp_ResponseMsg: %s\n", pResponse->psp_ResponseMsg);
printf("psp_TransactionId: %s\n", pResponse->psp_TransactionId);
printf("psp_Session3p: %s\n", pResponse->psp_Session3p);
printf("psp_FrontPSP_URL: %s\n", pResponse->psp_FrontPSP_URL);
printf("psp_BarCode: %s\n", pResponse->psp_BarCode);
printf("psp_MerchantId: %s\n", pResponse->psp_MerchantId);
printf("psp_MerchTxRef: %s\n", pResponse->psp_MerchTxRef);
printf("psp_MerchOrderId: %s\n", pResponse->psp_MerchOrderId);
printf("psp_Amount: %s\n", pResponse->psp_Amount);
printf("psp_Currency: %s\n", pResponse->psp_Currency);
printf("psp_Country: %s\n", pResponse->psp_Country);
printf("psp_Product: %s\n", pResponse->psp_Product);
printf("psp_PosDateTime: %s\n", pResponse->psp_PosDateTime);
printf("psp_CreatedAt: %s\n", pResponse->psp_CreatedAt);
