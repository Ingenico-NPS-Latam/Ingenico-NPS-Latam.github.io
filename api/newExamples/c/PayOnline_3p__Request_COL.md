#include <ctype.h>
#include <stdio.h>
#include <stdlib.h>
#include <string.h>
#include <unistd.h>
#include <time.h>
#include <stdbool.h>
#include <stddef.h>

#include <npsSdk.h>

int main(int argc, char **argv) {
    setEnvironment(SANDBOX_ENV);

    PAY_ONLINE_3P_REQ_STRUCT Request, *pRequest;
    PAY_ONLINE_3P_RESP_STRUCT Response, *pResponse;

    pRequest = &Request;
    memset(pRequest, 0, sizeof(PAY_ONLINE_3P_REQ_STRUCT));

    pRequest->psp_Version = malloc(strlen('2.2')+1);
    strcpy(pRequest->psp_Version, '2.2');

    pRequest->psp_MerchantId = malloc(strlen('sdk_test')+1);
    strcpy(pRequest->psp_MerchantId, 'sdk_test');

    pRequest->psp_TxSource = malloc(strlen('WEB')+1);
    strcpy(pRequest->psp_TxSource, 'WEB');

    pRequest->psp_MerchTxRef = malloc(strlen('ORDER76666-3')+1);
    strcpy(pRequest->psp_MerchTxRef, 'ORDER76666-3');

    pRequest->psp_MerchOrderId = malloc(strlen('ORDER76666')+1);
    strcpy(pRequest->psp_MerchOrderId, 'ORDER76666');

    pRequest->psp_ReturnURL = malloc(strlen('http://localhost/')+1);
    strcpy(pRequest->psp_ReturnURL, 'http://localhost/');

    pRequest->psp_FrmLanguage = malloc(strlen('es_AR')+1);
    strcpy(pRequest->psp_FrmLanguage, 'es_AR');

    pRequest->psp_Amount = malloc(strlen('1360000')+1);
    strcpy(pRequest->psp_Amount, '1360000');

    pRequest->psp_NumPayments = malloc(strlen('1')+1);
    strcpy(pRequest->psp_NumPayments, '1');

    pRequest->psp_Currency = malloc(strlen('170')+1);
    strcpy(pRequest->psp_Currency, '170');

    pRequest->psp_Country = malloc(strlen('COL')+1);
    strcpy(pRequest->psp_Country, 'COL');

    pRequest->psp_Product = malloc(strlen('14')+1);
    strcpy(pRequest->psp_Product, '14');

    pRequest->psp_PosDateTime = malloc(strlen('2019-12-01 12:00:00')+1);
    strcpy(pRequest->psp_PosDateTime, '2019-12-01 12:00:00');

    AMOUNT_ADDITIONAL_DETAILS_REQUEST_STRUCT AmountAdditionalDetails, *AmountAdditionalDetails;
    pAmountAdditionalDetails = &AmountAdditionalDetails;
    memset(ptr, 0, sizeof(AMOUNT_ADDITIONAL_DETAILS_REQUEST_STRUCT);

    pAmountAdditionalDetails->Tip = malloc(strlen('20')+1);
    strcpy(pAmountAdditionalDetails->Tip, '20');

    pAmountAdditionalDetails->Discount = malloc(strlen('1')+1);
    strcpy(pAmountAdditionalDetails->Discount, '1');

    ARRAYOF_TAXESREQUESTSTRUCT *pTaxes;
    pTaxes = (ARRAYOF_TAXESREQUESTSTRUCT*)malloc(sizeof(ARRAYOF_TAXESREQUESTSTRUCT));
    memset(pTaxes, 0, sizeof(ARRAYOF_TAXESREQUESTSTRUCT));
    pTaxes->__size=2;

    TAXES_REQUEST_STRUCT *ptr;
    pTaxes->__ptr=(TAXES_REQUEST_STRUCT *)malloc(sizeof(TAXES_REQUEST_STRUCT *)*2);

    for (int i = 0; i < pTaxes->__size; ++i) {
    ptr=(TAXES_REQUEST_STRUCT *)malloc(sizeof(TAXES_REQUEST_STRUCT));
    memset(ptr, 0, sizeof(TAXES_REQUEST_STRUCT));

    ptr->TypeId = malloc(strlen('100')+1);
    strcpy(ptr->TypeId, '100');

    ptr->Amount = malloc(strlen('200000')+1);
    strcpy(ptr->Amount, '200000');

    ptr->TypeId = malloc(strlen('501')+1);
    strcpy(ptr->TypeId, '501');

    ptr->Amount = malloc(strlen('160000')+1);
    strcpy(ptr->Amount, '160000');

    ptr->Rate = malloc(strlen('1600')+1);
    strcpy(ptr->Rate, '1600');

    ptr->BaseAmount = malloc(strlen('1000000')+1);
    strcpy(ptr->BaseAmount, '1000000');

    pTaxes->__ptr[i]=ptr;
    }

    pAmountAdditionalDetails->Taxes=pTaxes;

    pRequest->psp_AmountAdditionalDetails = pAmountAdditionalDetails;


    pResponse = &Response;

    showRequest(PAY_ONLINE_3P_TYPE,(char *)pRequest);
    sendRequest(PAY_ONLINE_3P_TYPE, YOUR_SECRET_KEY, (char *)pRequest, pResponse);
    showResponse(PAY_ONLINE_3P_TYPE,(char *)pResponse);
}
