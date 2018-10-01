QUERY_CARD_NUMBER_RESP_STRUCT Response, *pResponse;
pResponse = &Response;

printf("psp_ResponseCod: %s\n", pResponse->psp_ResponseCod);
printf("psp_ResponseMsg: %s\n", pResponse->psp_ResponseMsg);
printf("psp_MerchantId: %s\n", pResponse->psp_MerchantId);
printf("psp_QueryCriteria: %s\n", pResponse->psp_QueryCriteria);
printf("psp_QueryCriteriaId: %s\n", pResponse->psp_QueryCriteriaId);
printf("psp_PosDateTime: %s\n", pResponse->psp_PosDateTime);
printf("psp_CardNumber: %s\n", pResponse->psp_CardNumber);
