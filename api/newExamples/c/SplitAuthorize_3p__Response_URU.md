SPLIT_AUTHORIZE_3P_RESP_STRUCT Response, *pResponse;
pResponse = &Response;

printf("psp_ResponseCod: %s\n", pResponse->psp_ResponseCod);
printf("psp_ResponseMsg: %s\n", pResponse->psp_ResponseMsg);
printf("psp_TransactionId: %s\n", pResponse->psp_TransactionId);
printf("psp_Session3p: %s\n", pResponse->psp_Session3p);
printf("psp_FrontPSP_URL: %s\n", pResponse->psp_FrontPSP_URL);
printf("psp_MerchantId: %s\n", pResponse->psp_MerchantId);
printf("psp_MerchTxRef: %s\n", pResponse->psp_MerchTxRef);
printf("psp_MerchOrderId: %s\n", pResponse->psp_MerchOrderId);
printf("psp_Amount: %s\n", pResponse->psp_Amount);
printf("psp_Currency: %s\n", pResponse->psp_Currency);
printf("psp_Country: %s\n", pResponse->psp_Country);
printf("psp_Product: %s\n", pResponse->psp_Product);
printf("psp_PosDateTime: %s\n", pResponse->psp_PosDateTime);

ARRAYOF_RESPUESTASTRUCT_SPLITAUTHORIZE_3P_TRANSACTIONS *pTransactions;
pTransactions = pResponse->psp_Transactions;

for (i = 0; i < pTransactions->__size; i++) {
RESPUESTASTRUCT_SPLITAUTHORIZE_3P_TRANSACTIONS *pTransactions0;
pTransactions0 = pTransactions->__ptr[0];
printf("psp_MerchantId: %s\n", pTransactions0->psp_MerchantId);
printf("psp_TransactionId: %s\n", pTransactions0->psp_TransactionId);
printf("psp_MerchTxRef: %s\n", pTransactions0->psp_MerchTxRef);
printf("psp_Product: %s\n", pTransactions0->psp_Product);
printf("psp_Amount: %s\n", pTransactions0->psp_Amount);
printf("psp_NumPayments: %s\n", pTransactions0->psp_NumPayments);
printf("psp_CreatedAt: %s\n", pTransactions0->psp_CreatedAt);

RESPUESTASTRUCT_SPLITAUTHORIZE_3P_TRANSACTIONS *pTransactions1;
pTransactions1 = pTransactions->__ptr[1];
printf("psp_MerchantId: %s\n", pTransactions1->psp_MerchantId);
printf("psp_TransactionId: %s\n", pTransactions1->psp_TransactionId);
printf("psp_MerchTxRef: %s\n", pTransactions1->psp_MerchTxRef);
printf("psp_Product: %s\n", pTransactions1->psp_Product);
printf("psp_Amount: %s\n", pTransactions1->psp_Amount);
printf("psp_NumPayments: %s\n", pTransactions1->psp_NumPayments);
printf("psp_CreatedAt: %s\n", pTransactions1->psp_CreatedAt);

}
