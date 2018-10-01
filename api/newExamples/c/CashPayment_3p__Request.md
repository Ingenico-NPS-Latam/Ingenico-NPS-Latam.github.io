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

    CASH_PAYMENT_3P_REQ_STRUCT Request, *pRequest;
    CASH_PAYMENT_3P_RESP_STRUCT Response, *pResponse;

    pRequest = &Request;
    memset(pRequest, 0, sizeof(CASH_PAYMENT_3P_REQ_STRUCT));

    pRequest->psp_Version = malloc(strlen('2.2')+1);
    strcpy(pRequest->psp_Version, '2.2');

    pRequest->psp_MerchantId = malloc(strlen('sdk_test')+1);
    strcpy(pRequest->psp_MerchantId, 'sdk_test');

    pRequest->psp_TxSource = malloc(strlen('WEB')+1);
    strcpy(pRequest->psp_TxSource, 'WEB');

    pRequest->psp_MerchTxRef = malloc(strlen('ORDER32145-3')+1);
    strcpy(pRequest->psp_MerchTxRef, 'ORDER32145-3');

    pRequest->psp_MerchOrderId = malloc(strlen('ORDER32145')+1);
    strcpy(pRequest->psp_MerchOrderId, 'ORDER32145');

    pRequest->psp_ReturnURL = malloc(strlen('http://localhost/')+1);
    strcpy(pRequest->psp_ReturnURL, 'http://localhost/');

    pRequest->psp_FrmLanguage = malloc(strlen('es_AR')+1);
    strcpy(pRequest->psp_FrmLanguage, 'es_AR');

    pRequest->psp_Amount = malloc(strlen('15050')+1);
    strcpy(pRequest->psp_Amount, '15050');

    pRequest->psp_Currency = malloc(strlen('032')+1);
    strcpy(pRequest->psp_Currency, '032');

    pRequest->psp_Country = malloc(strlen('ARG')+1);
    strcpy(pRequest->psp_Country, 'ARG');

    pRequest->psp_Product = malloc(strlen('301')+1);
    strcpy(pRequest->psp_Product, '301');

    pRequest->psp_PosDateTime = malloc(strlen('2019-12-01 12:00:00')+1);
    strcpy(pRequest->psp_PosDateTime, '2019-12-01 12:00:00');

    pRequest->psp_FirstExpDate = malloc(strlen('2020-01-01')+1);
    strcpy(pRequest->psp_FirstExpDate, '2020-01-01');


    pResponse = &Response;

    showRequest(CASH_PAYMENT_3P_TYPE,(char *)pRequest);
    sendRequest(CASH_PAYMENT_3P_TYPE, YOUR_SECRET_KEY, (char *)pRequest, pResponse);
    showResponse(CASH_PAYMENT_3P_TYPE,(char *)pResponse);
}
