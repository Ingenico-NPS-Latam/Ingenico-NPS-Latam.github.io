AUTHORIZE_2P_RESP_STRUCT Response, *pResponse;
pResponse = &Response;

printf("psp_ResponseCod: %s\n", pResponse->psp_ResponseCod);
printf("psp_ResponseMsg: %s\n", pResponse->psp_ResponseMsg);
printf("psp_ResponseExtended: %s\n", pResponse->psp_ResponseExtended);
printf("psp_TransactionId: %s\n", pResponse->psp_TransactionId);
printf("psp_MerchantId: %s\n", pResponse->psp_MerchantId);
printf("psp_MerchTxRef: %s\n", pResponse->psp_MerchTxRef);
printf("psp_MerchOrderId: %s\n", pResponse->psp_MerchOrderId);
printf("psp_Amount: %s\n", pResponse->psp_Amount);
printf("psp_NumPayments: %s\n", pResponse->psp_NumPayments);
printf("psp_Currency: %s\n", pResponse->psp_Currency);
printf("psp_Country: %s\n", pResponse->psp_Country);
printf("psp_Product: %s\n", pResponse->psp_Product);
printf("psp_CardNumber: %s\n", pResponse->psp_CardNumber);
printf("psp_CardExpDate: %s\n", pResponse->psp_CardExpDate);
printf("psp_AuthorizationCode: %s\n", pResponse->psp_AuthorizationCode);
printf("psp_SequenceNumber: %s\n", pResponse->psp_SequenceNumber);
printf("psp_ClTrnId: %s\n", pResponse->psp_ClTrnId);
printf("psp_ClExternalMerchant: %s\n", pResponse->psp_ClExternalMerchant);
printf("psp_ClResponseCod: %s\n", pResponse->psp_ClResponseCod);
printf("psp_ClResponseMsg: %s\n", pResponse->psp_ClResponseMsg);
printf("psp_PosDateTime: %s\n", pResponse->psp_PosDateTime);
printf("psp_Plan: %s\n", pResponse->psp_Plan);
printf("psp_CreatedAt: %s\n", pResponse->psp_CreatedAt);

AMOUNT_ADDITIONAL_DETAILS_RESPONSE_STRUCT *pAmountAdditionalDetailsResponse;
pAmountAdditionalDetailsResponse = pResponse->psp_AmountAdditionalDetails;
printf("Tip: %s\n", pAmountAdditionalDetailsResponse->Tip);
printf("Discount: %s\n", pAmountAdditionalDetailsResponse->Discount);

ARRAYOF_TAXES_RESPONSE_STRUCT *pTaxes;
pTaxes = pAmountAdditionalDetailsResponse->Taxes;

for (i = 0; i < pTaxes->__size; i++) {
TAXES_RESPONSE_STRUCT *pTaxes0;
pTaxes0 = pTaxes->__ptr[0];
printf("TypeId: %s\n", pTaxes0->TypeId);
printf("TypeDescription: %s\n", pTaxes0->TypeDescription);
printf("Amount: %s\n", pTaxes0->Amount);
printf("Rate: %s\n", pTaxes0->Rate);
printf("BaseAmount: %s\n", pTaxes0->BaseAmount);
printf("AppliedAmount: %s\n", pTaxes0->AppliedAmount);
printf("Remarks: %s\n", pTaxes0->Remarks);

}

FRAUD_SCREENING_RESULT_STRUCT *pFraudScreeningResultResponse;
pFraudScreeningResultResponse = pResponse->psp_FraudScreeningResult;
printf("ResultCode: %s\n", pFraudScreeningResultResponse->ResultCode);
printf("ResultDescription: %s\n", pFraudScreeningResultResponse->ResultDescription);

VERIFICATION_SERVICES_RESULT_STRUCT *pVerificationServicesResultResponse;
pVerificationServicesResultResponse = pResponse->psp_VerificationServicesResult;
printf("ResultCodeCardSecurityCode: %s\n", pVerificationServicesResultResponse->ResultCodeCardSecurityCode);
printf("ResultCodeBillingAddress: %s\n", pVerificationServicesResultResponse->ResultCodeBillingAddress);
printf("ResultCodeBillingAddressZipCode: %s\n", pVerificationServicesResultResponse->ResultCodeBillingAddressZipCode);
printf("ResultCodeBillingPersonIDType: %s\n", pVerificationServicesResultResponse->ResultCodeBillingPersonIDType);
printf("ResultCodeBillingPersonIDNumber: %s\n", pVerificationServicesResultResponse->ResultCodeBillingPersonIDNumber);
printf("ResultCodeBillingPersonDateOfBirth: %s\n", pVerificationServicesResultResponse->ResultCodeBillingPersonDateOfBirth);
printf("ResultCodeBillingPersonName: %s\n", pVerificationServicesResultResponse->ResultCodeBillingPersonName);
printf("ResultCodeBillingPersonPhoneNumber1: %s\n", pVerificationServicesResultResponse->ResultCodeBillingPersonPhoneNumber1);
printf("ResultCodeCustomerEmailAddress: %s\n", pVerificationServicesResultResponse->ResultCodeCustomerEmailAddress);
