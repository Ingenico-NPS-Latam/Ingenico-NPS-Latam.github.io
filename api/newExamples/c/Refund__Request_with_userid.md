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

    REFUND_REQ_STRUCT Request, *pRequest;
    REFUND_RESP_STRUCT Response, *pResponse;

    pRequest = &Request;
    memset(pRequest, 0, sizeof(REFUND_REQ_STRUCT));

    pRequest->psp_Version = malloc(strlen('2.2')+1);
    strcpy(pRequest->psp_Version, '2.2');

    pRequest->psp_MerchantId = malloc(strlen('sdk_test')+1);
    strcpy(pRequest->psp_MerchantId, 'sdk_test');

    pRequest->psp_TxSource = malloc(strlen('WEB')+1);
    strcpy(pRequest->psp_TxSource, 'WEB');

    pRequest->psp_MerchTxRef = malloc(strlen('ORDER66666-3')+1);
    strcpy(pRequest->psp_MerchTxRef, 'ORDER66666-3');

    pRequest->psp_TransactionId_Orig = malloc(strlen('2693348')+1);
    strcpy(pRequest->psp_TransactionId_Orig, '2693348');

    pRequest->psp_AmountToRefund = malloc(strlen('15050')+1);
    strcpy(pRequest->psp_AmountToRefund, '15050');

    pRequest->psp_UserId = malloc(strlen('john_doe')+1);
    strcpy(pRequest->psp_UserId, 'john_doe');

    pRequest->psp_PosDateTime = malloc(strlen('2019-12-01 12:00:00')+1);
    strcpy(pRequest->psp_PosDateTime, '2019-12-01 12:00:00');


    pResponse = &Response;

    showRequest(REFUND_TYPE,(char *)pRequest);
    sendRequest(REFUND_TYPE, YOUR_SECRET_KEY, (char *)pRequest, pResponse);
    showResponse(REFUND_TYPE,(char *)pResponse);
}
