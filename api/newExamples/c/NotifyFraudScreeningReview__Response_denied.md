NOTIFY_FRAUD_SCREENING_REVIEW_RESP_STRUCT Response, *pResponse;
pResponse = &Response;

printf("psp_ResponseCod: %s\n", pResponse->psp_ResponseCod);
printf("psp_ResponseMsg: %s\n", pResponse->psp_ResponseMsg);
printf("psp_MerchantId: %s\n", pResponse->psp_MerchantId);
printf("psp_Criteria: %s\n", pResponse->psp_Criteria);
printf("psp_CriteriaId: %s\n", pResponse->psp_CriteriaId);
printf("psp_PosDateTime: %s\n", pResponse->psp_PosDateTime);
