QUERY_TXS_RESP_STRUCT Response, *pResponse;
pResponse = &Response;

printf("psp_ResponseCod: %s\n", pResponse->psp_ResponseCod);
printf("psp_ResponseMsg: %s\n", pResponse->psp_ResponseMsg);
printf("psp_MerchantId: %s\n", pResponse->psp_MerchantId);
printf("psp_QueryCriteria: %s\n", pResponse->psp_QueryCriteria);
printf("psp_QueryCriteriaId: %s\n", pResponse->psp_QueryCriteriaId);
printf("psp_PosDateTime: %s\n", pResponse->psp_PosDateTime);

ARRAYOF_RESPUESTASTRUCT_QUERYTXS_TRANSACTIONS *pTransactions;
pTransactions = pResponse->psp_Transactions;

for (i = 0; i < pTransactions->__size; i++) {
RESPUESTASTRUCT_QUERYTXS_TRANSACTIONS *pTransactions0;
pTransactions0 = pTransactions->__ptr[0];
printf("psp_ResponseCod: %s\n", pTransactions0->psp_ResponseCod);
printf("psp_ResponseMsg: %s\n", pTransactions0->psp_ResponseMsg);
printf("psp_ResponseExtended: %s\n", pTransactions0->psp_ResponseExtended);
printf("psp_TransactionId: %s\n", pTransactions0->psp_TransactionId);
printf("psp_MerchantId: %s\n", pTransactions0->psp_MerchantId);
printf("psp_TxSource: %s\n", pTransactions0->psp_TxSource);
printf("psp_Operation: %s\n", pTransactions0->psp_Operation);
printf("psp_MerchTxRef: %s\n", pTransactions0->psp_MerchTxRef);
printf("psp_MerchOrderId: %s\n", pTransactions0->psp_MerchOrderId);
printf("psp_Amount: %s\n", pTransactions0->psp_Amount);
printf("psp_NumPayments: %s\n", pTransactions0->psp_NumPayments);
printf("psp_Currency: %s\n", pTransactions0->psp_Currency);
printf("psp_Country: %s\n", pTransactions0->psp_Country);
printf("psp_Product: %s\n", pTransactions0->psp_Product);
printf("psp_AuthorizationCode: %s\n", pTransactions0->psp_AuthorizationCode);
printf("psp_BatchNro: %s\n", pTransactions0->psp_BatchNro);
printf("psp_TicketNumber: %s\n", pTransactions0->psp_TicketNumber);
printf("psp_CardNumber_FSD: %s\n", pTransactions0->psp_CardNumber_FSD);
printf("psp_CardNumber_LFD: %s\n", pTransactions0->psp_CardNumber_LFD);
printf("psp_CardMask: %s\n", pTransactions0->psp_CardMask);
printf("psp_ClExternalMerchant: %s\n", pTransactions0->psp_ClExternalMerchant);
printf("psp_ClExternalTerminal: %s\n", pTransactions0->psp_ClExternalTerminal);
printf("psp_ClResponseCod: %s\n", pTransactions0->psp_ClResponseCod);
printf("psp_ClResponseMsg: %s\n", pTransactions0->psp_ClResponseMsg);
printf("psp_PosDateTime: %s\n", pTransactions0->psp_PosDateTime);
printf("psp_CreatedAt: %s\n", pTransactions0->psp_CreatedAt);

FRAUD_SCREENING_RESULT_STRUCT *pFraudScreeningResultResponse;
pFraudScreeningResultResponse = pTransactions0->psp_FraudScreeningResult;
printf("ResultCode: %s\n", pFraudScreeningResultResponse->ResultCode);
printf("ResultDescription: %s\n", pFraudScreeningResultResponse->ResultDescription);

VERIFICATION_SERVICES_RESULT_STRUCT *pVerificationServicesResultResponse;
pVerificationServicesResultResponse = pTransactions0->psp_VerificationServicesResult;
printf("ResultCodeCardSecurityCode: %s\n", pVerificationServicesResultResponse->ResultCodeCardSecurityCode);
printf("ResultCodeBillingAddress: %s\n", pVerificationServicesResultResponse->ResultCodeBillingAddress);
printf("ResultCodeBillingAddressZipCode: %s\n", pVerificationServicesResultResponse->ResultCodeBillingAddressZipCode);
printf("ResultCodeBillingPersonIDType: %s\n", pVerificationServicesResultResponse->ResultCodeBillingPersonIDType);
printf("ResultCodeBillingPersonIDNumber: %s\n", pVerificationServicesResultResponse->ResultCodeBillingPersonIDNumber);
printf("ResultCodeBillingPersonDateOfBirth: %s\n", pVerificationServicesResultResponse->ResultCodeBillingPersonDateOfBirth);
printf("ResultCodeBillingPersonName: %s\n", pVerificationServicesResultResponse->ResultCodeBillingPersonName);
printf("ResultCodeBillingPersonPhoneNumber1: %s\n", pVerificationServicesResultResponse->ResultCodeBillingPersonPhoneNumber1);
printf("ResultCodeCustomerEmailAddress: %s\n", pVerificationServicesResultResponse->ResultCodeCustomerEmailAddress);

RESPUESTASTRUCT_QUERYTXS_TRANSACTIONS *pTransactions1;
pTransactions1 = pTransactions->__ptr[1];
printf("psp_ResponseCod: %s\n", pTransactions1->psp_ResponseCod);
printf("psp_ResponseMsg: %s\n", pTransactions1->psp_ResponseMsg);
printf("psp_ResponseExtended: %s\n", pTransactions1->psp_ResponseExtended);
printf("psp_TransactionId: %s\n", pTransactions1->psp_TransactionId);
printf("psp_MerchantId: %s\n", pTransactions1->psp_MerchantId);
printf("psp_TxSource: %s\n", pTransactions1->psp_TxSource);
printf("psp_Operation: %s\n", pTransactions1->psp_Operation);
printf("psp_MerchTxRef: %s\n", pTransactions1->psp_MerchTxRef);
printf("psp_MerchOrderId: %s\n", pTransactions1->psp_MerchOrderId);
printf("psp_Amount: %s\n", pTransactions1->psp_Amount);
printf("psp_NumPayments: %s\n", pTransactions1->psp_NumPayments);
printf("psp_Currency: %s\n", pTransactions1->psp_Currency);
printf("psp_Country: %s\n", pTransactions1->psp_Country);
printf("psp_Product: %s\n", pTransactions1->psp_Product);
printf("psp_AuthorizationCode: %s\n", pTransactions1->psp_AuthorizationCode);
printf("psp_BatchNro: %s\n", pTransactions1->psp_BatchNro);
printf("psp_TicketNumber: %s\n", pTransactions1->psp_TicketNumber);
printf("psp_CardNumber_FSD: %s\n", pTransactions1->psp_CardNumber_FSD);
printf("psp_CardNumber_LFD: %s\n", pTransactions1->psp_CardNumber_LFD);
printf("psp_CardMask: %s\n", pTransactions1->psp_CardMask);
printf("psp_ClExternalMerchant: %s\n", pTransactions1->psp_ClExternalMerchant);
printf("psp_ClExternalTerminal: %s\n", pTransactions1->psp_ClExternalTerminal);
printf("psp_ClResponseCod: %s\n", pTransactions1->psp_ClResponseCod);
printf("psp_ClResponseMsg: %s\n", pTransactions1->psp_ClResponseMsg);
printf("psp_PosDateTime: %s\n", pTransactions1->psp_PosDateTime);
printf("psp_CreatedAt: %s\n", pTransactions1->psp_CreatedAt);

FRAUD_SCREENING_RESULT_STRUCT *pFraudScreeningResultResponse;
pFraudScreeningResultResponse = pTransactions1->psp_FraudScreeningResult;
printf("ResultCode: %s\n", pFraudScreeningResultResponse->ResultCode);
printf("ResultDescription: %s\n", pFraudScreeningResultResponse->ResultDescription);

VERIFICATION_SERVICES_RESULT_STRUCT *pVerificationServicesResultResponse;
pVerificationServicesResultResponse = pTransactions1->psp_VerificationServicesResult;
printf("ResultCodeCardSecurityCode: %s\n", pVerificationServicesResultResponse->ResultCodeCardSecurityCode);
printf("ResultCodeBillingAddress: %s\n", pVerificationServicesResultResponse->ResultCodeBillingAddress);
printf("ResultCodeBillingAddressZipCode: %s\n", pVerificationServicesResultResponse->ResultCodeBillingAddressZipCode);
printf("ResultCodeBillingPersonIDType: %s\n", pVerificationServicesResultResponse->ResultCodeBillingPersonIDType);
printf("ResultCodeBillingPersonIDNumber: %s\n", pVerificationServicesResultResponse->ResultCodeBillingPersonIDNumber);
printf("ResultCodeBillingPersonDateOfBirth: %s\n", pVerificationServicesResultResponse->ResultCodeBillingPersonDateOfBirth);
printf("ResultCodeBillingPersonName: %s\n", pVerificationServicesResultResponse->ResultCodeBillingPersonName);
printf("ResultCodeBillingPersonPhoneNumber1: %s\n", pVerificationServicesResultResponse->ResultCodeBillingPersonPhoneNumber1);
printf("ResultCodeCustomerEmailAddress: %s\n", pVerificationServicesResultResponse->ResultCodeCustomerEmailAddress);

}
