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

    PAY_ONLINE_2P_REQ_STRUCT Request, *pRequest;
    PAY_ONLINE_2P_RESP_STRUCT Response, *pResponse;

    pRequest = &Request;
    memset(pRequest, 0, sizeof(PAY_ONLINE_2P_REQ_STRUCT));

    pRequest->psp_Version = malloc(strlen('2.2')+1);
    strcpy(pRequest->psp_Version, '2.2');

    pRequest->psp_MerchantId = malloc(strlen('sdk_test')+1);
    strcpy(pRequest->psp_MerchantId, 'sdk_test');

    pRequest->psp_TxSource = malloc(strlen('WEB')+1);
    strcpy(pRequest->psp_TxSource, 'WEB');

    pRequest->psp_MerchTxRef = malloc(strlen('ORDER69461-3')+1);
    strcpy(pRequest->psp_MerchTxRef, 'ORDER69461-3');

    pRequest->psp_MerchOrderId = malloc(strlen('ORDER69461')+1);
    strcpy(pRequest->psp_MerchOrderId, 'ORDER69461');

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

    pRequest->psp_CardSecurityCode = malloc(strlen('325')+1);
    strcpy(pRequest->psp_CardSecurityCode, '325');

    pRequest->psp_PosDateTime = malloc(strlen('2019-12-01 12:00:00')+1);
    strcpy(pRequest->psp_PosDateTime, '2019-12-01 12:00:00');


    pResponse = &Response;

    showRequest(PAY_ONLINE_2P_TYPE,(char *)pRequest);
    sendRequest(PAY_ONLINE_2P_TYPE, YOUR_SECRET_KEY, (char *)pRequest, pResponse);
    showResponse(PAY_ONLINE_2P_TYPE,(char *)pResponse);
}
