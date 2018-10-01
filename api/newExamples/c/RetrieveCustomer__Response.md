RETRIEVE_CUSTOMER_RESP_STRUCT Response, *pResponse;
pResponse = &Response;

printf("psp_ResponseCod: %s\n", pResponse->psp_ResponseCod);
printf("psp_ResponseMsg: %s\n", pResponse->psp_ResponseMsg);
printf("psp_MerchantId: %s\n", pResponse->psp_MerchantId);
printf("psp_CustomerId: %s\n", pResponse->psp_CustomerId);
printf("psp_EmailAddress: %s\n", pResponse->psp_EmailAddress);
printf("psp_AlternativeEmailAddress: %s\n", pResponse->psp_AlternativeEmailAddress);
printf("psp_AccountID: %s\n", pResponse->psp_AccountID);
printf("psp_AccountCreatedAt: %s\n", pResponse->psp_AccountCreatedAt);
printf("psp_PosDateTime: %s\n", pResponse->psp_PosDateTime);
