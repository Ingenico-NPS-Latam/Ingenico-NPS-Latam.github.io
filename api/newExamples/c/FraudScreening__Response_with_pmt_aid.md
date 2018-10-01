FRAUD_SCREENING_RESP_STRUCT Response, *pResponse;
pResponse = &Response;

printf("psp_ResponseCod: %s\n", pResponse->psp_ResponseCod);
printf("psp_ResponseMsg: %s\n", pResponse->psp_ResponseMsg);

FRAUD_SCREENING_RESP_STRUCT *pResultResponse;
pResultResponse = pResponse->psp_Result;
printf("ResultCode: %s\n", pResultResponse->ResultCode);
printf("ResultDescription: %s\n", pResultResponse->ResultDescription);
printf("psp_OrderId: %s\n", pResponse->psp_OrderId);
printf("psp_MerchantId: %s\n", pResponse->psp_MerchantId);
printf("psp_MerchTxRef: %s\n", pResponse->psp_MerchTxRef);
printf("psp_MerchOrderId: %s\n", pResponse->psp_MerchOrderId);
printf("psp_Amount: %s\n", pResponse->psp_Amount);
printf("psp_NumPayments: %s\n", pResponse->psp_NumPayments);
printf("psp_Currency: %s\n", pResponse->psp_Currency);
printf("psp_Country: %s\n", pResponse->psp_Country);
printf("psp_Product: %s\n", pResponse->psp_Product);
printf("psp_CardExpDate: %s\n", pResponse->psp_CardExpDate);
printf("psp_PosDateTime: %s\n", pResponse->psp_PosDateTime);
printf("psp_CreatedAt: %s\n", pResponse->psp_CreatedAt);
