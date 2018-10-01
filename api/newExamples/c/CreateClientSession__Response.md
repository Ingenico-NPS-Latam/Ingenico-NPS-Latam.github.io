CREATE_CLIENT_SESSION_RESP_STRUCT Response, *pResponse;
pResponse = &Response;

printf("psp_ResponseCod: %s\n", pResponse->psp_ResponseCod);
printf("psp_ResponseMsg: %s\n", pResponse->psp_ResponseMsg);
printf("psp_MerchantId: %s\n", pResponse->psp_MerchantId);
printf("psp_ClientSession: %s\n", pResponse->psp_ClientSession);
printf("psp_PosDateTime: %s\n", pResponse->psp_PosDateTime);
printf("psp_CreatedAt: %s\n", pResponse->psp_CreatedAt);
