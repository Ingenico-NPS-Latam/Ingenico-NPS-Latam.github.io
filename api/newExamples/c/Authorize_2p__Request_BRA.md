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

    AUTHORIZE_2P_REQ_STRUCT Request, *pRequest;
    AUTHORIZE_2P_RESP_STRUCT Response, *pResponse;

    pRequest = &Request;
    memset(pRequest, 0, sizeof(AUTHORIZE_2P_REQ_STRUCT));

    pRequest->psp_Version = malloc(strlen('2.2')+1);
    strcpy(pRequest->psp_Version, '2.2');

    pRequest->psp_MerchantId = malloc(strlen('psp_test')+1);
    strcpy(pRequest->psp_MerchantId, 'psp_test');

    pRequest->psp_TxSource = malloc(strlen('WEB')+1);
    strcpy(pRequest->psp_TxSource, 'WEB');

    pRequest->psp_MerchTxRef = malloc(strlen('ORDERX1466Xz-3')+1);
    strcpy(pRequest->psp_MerchTxRef, 'ORDERX1466Xz-3');

    pRequest->psp_MerchOrderId = malloc(strlen('ORDERX1466Xz')+1);
    strcpy(pRequest->psp_MerchOrderId, 'ORDERX1466Xz');

    pRequest->psp_Amount = malloc(strlen('1200000')+1);
    strcpy(pRequest->psp_Amount, '1200000');

    pRequest->psp_NumPayments = malloc(strlen('3')+1);
    strcpy(pRequest->psp_NumPayments, '3');

    pRequest->psp_CardSecurityCode = malloc(strlen('321')+1);
    strcpy(pRequest->psp_CardSecurityCode, '321');

    pRequest->psp_Currency = malloc(strlen('986')+1);
    strcpy(pRequest->psp_Currency, '986');

    pRequest->psp_Country = malloc(strlen('BRA')+1);
    strcpy(pRequest->psp_Country, 'BRA');

    pRequest->psp_Product = malloc(strlen('5')+1);
    strcpy(pRequest->psp_Product, '5');

    pRequest->psp_Plan = malloc(strlen('CC')+1);
    strcpy(pRequest->psp_Plan, 'CC');

    pRequest->psp_CardNumber = malloc(strlen('5453010000083303')+1);
    strcpy(pRequest->psp_CardNumber, '5453010000083303');

    pRequest->psp_CardExpDate = malloc(strlen('1904')+1);
    strcpy(pRequest->psp_CardExpDate, '1904');

    pRequest->psp_PosDateTime = malloc(strlen('2017-03-31 16:14:06')+1);
    strcpy(pRequest->psp_PosDateTime, '2017-03-31 16:14:06');

    pRequest->psp_ForceProcessingMethod = malloc(strlen('16')+1);
    strcpy(pRequest->psp_ForceProcessingMethod, '16');

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
    pTaxes->__size=1;

    TAXES_REQUEST_STRUCT *ptr;
    pTaxes->__ptr=(TAXES_REQUEST_STRUCT *)malloc(sizeof(TAXES_REQUEST_STRUCT *)*1);

    for (int i = 0; i < pTaxes->__size; ++i) {
    ptr=(TAXES_REQUEST_STRUCT *)malloc(sizeof(TAXES_REQUEST_STRUCT));
    memset(ptr, 0, sizeof(TAXES_REQUEST_STRUCT));

    ptr->TypeId = malloc(strlen('100')+1);
    strcpy(ptr->TypeId, '100');

    ptr->Amount = malloc(strlen('200000')+1);
    strcpy(ptr->Amount, '200000');

    pTaxes->__ptr[i]=ptr;
    }

    pAmountAdditionalDetails->Taxes=pTaxes;

    pRequest->psp_AmountAdditionalDetails = pAmountAdditionalDetails;


    pResponse = &Response;

    showRequest(AUTHORIZE_2P_TYPE,(char *)pRequest);
    sendRequest(AUTHORIZE_2P_TYPE, YOUR_SECRET_KEY, (char *)pRequest, pResponse);
    showResponse(AUTHORIZE_2P_TYPE,(char *)pResponse);
}
