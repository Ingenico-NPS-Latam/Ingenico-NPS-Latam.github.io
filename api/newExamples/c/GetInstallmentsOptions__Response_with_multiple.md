GET_INSTALLMENTS_OPTIONS_RESP_STRUCT Response, *pResponse;
pResponse = &Response;

printf("psp_ResponseCod: %s\n", pResponse->psp_ResponseCod);
printf("psp_ResponseMsg: %s\n", pResponse->psp_ResponseMsg);
printf("psp_MerchantId: %s\n", pResponse->psp_MerchantId);
printf("psp_Amount: %s\n", pResponse->psp_Amount);
printf("psp_Product: %s\n", pResponse->psp_Product);
printf("psp_Currency: %s\n", pResponse->psp_Currency);
printf("psp_Country: %s\n", pResponse->psp_Country);
printf("psp_NumPayments: %s\n", pResponse->psp_NumPayments);

ARRAYOF_INSTALLMENTS_OPTIONS_STRUCT *pInstallmentsOptions;
pInstallmentsOptions = pResponse->psp_InstallmentsOptions;

for (i = 0; i < pInstallmentsOptions->__size; i++) {
INSTALLMENTS_OPTIONS_STRUCT *pInstallmentsOptions0;
pInstallmentsOptions0 = pInstallmentsOptions->__ptr[0];
printf("NumPayments: %s\n", pInstallmentsOptions0->NumPayments);
printf("InstallmentAmount: %s\n", pInstallmentsOptions0->InstallmentAmount);

}
printf("psp_PosDateTime: %s\n", pResponse->psp_PosDateTime);
