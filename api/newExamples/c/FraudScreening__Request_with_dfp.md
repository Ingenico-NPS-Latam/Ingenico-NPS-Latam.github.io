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

    FRAUD_SCREENING_REQ_STRUCT Request, *pRequest;
    FRAUD_SCREENING_RESP_STRUCT Response, *pResponse;

    pRequest = &Request;
    memset(pRequest, 0, sizeof(FRAUD_SCREENING_REQ_STRUCT));

    pRequest->psp_Version = malloc(strlen('2.2')+1);
    strcpy(pRequest->psp_Version, '2.2');

    pRequest->psp_MerchantId = malloc(strlen('sdk_test')+1);
    strcpy(pRequest->psp_MerchantId, 'sdk_test');

    pRequest->psp_TxSource = malloc(strlen('WEB')+1);
    strcpy(pRequest->psp_TxSource, 'WEB');

    pRequest->psp_MerchTxRef = malloc(strlen('ORDER66666-3')+1);
    strcpy(pRequest->psp_MerchTxRef, 'ORDER66666-3');

    pRequest->psp_MerchOrderId = malloc(strlen('ORDER66666')+1);
    strcpy(pRequest->psp_MerchOrderId, 'ORDER66666');

    pRequest->psp_Amount = malloc(strlen('15050')+1);
    strcpy(pRequest->psp_Amount, '15050');

    pRequest->psp_NumPayments = malloc(strlen('1')+1);
    strcpy(pRequest->psp_NumPayments, '1');

    pRequest->psp_Currency = malloc(strlen('032')+1);
    strcpy(pRequest->psp_Currency, '032');

    pRequest->psp_Country = malloc(strlen('ARG')+1);
    strcpy(pRequest->psp_Country, 'ARG');

    pRequest->psp_Product = malloc(strlen('14')+1);
    strcpy(pRequest->psp_Product, '14');

    pRequest->psp_CardNumber = malloc(strlen('4507990000000010')+1);
    strcpy(pRequest->psp_CardNumber, '4507990000000010');

    pRequest->psp_CardExpDate = malloc(strlen('1912')+1);
    strcpy(pRequest->psp_CardExpDate, '1912');

    pRequest->psp_PosDateTime = malloc(strlen('2019-12-01 12:00:00')+1);
    strcpy(pRequest->psp_PosDateTime, '2019-12-01 12:00:00');

    CUSTOMER_ADDITIONAL_DETAILS_STRUCT CustomerAdditionalDetails, *CustomerAdditionalDetails;
    pCustomerAdditionalDetails = &CustomerAdditionalDetails;
    memset(ptr, 0, sizeof(CUSTOMER_ADDITIONAL_DETAILS_STRUCT);

    pCustomerAdditionalDetails->DeviceFingerPrint = malloc(strlen('KJhKHKJgh7777kgh...')+1);
    strcpy(pCustomerAdditionalDetails->DeviceFingerPrint, 'KJhKHKJgh7777kgh...');

    pRequest->psp_CustomerAdditionalDetails = pCustomerAdditionalDetails;


    pResponse = &Response;

    showRequest(FRAUD_SCREENING_TYPE,(char *)pRequest);
    sendRequest(FRAUD_SCREENING_TYPE, YOUR_SECRET_KEY, (char *)pRequest, pResponse);
    showResponse(FRAUD_SCREENING_TYPE,(char *)pResponse);
}
