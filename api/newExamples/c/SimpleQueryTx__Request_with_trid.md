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

    SIMPLE_QUERY_TX_REQ_STRUCT Request, *pRequest;
    SIMPLE_QUERY_TX_RESP_STRUCT Response, *pResponse;

    pRequest = &Request;
    memset(pRequest, 0, sizeof(SIMPLE_QUERY_TX_REQ_STRUCT));

    pRequest->psp_Version = malloc(strlen('2.2')+1);
    strcpy(pRequest->psp_Version, '2.2');

    pRequest->psp_MerchantId = malloc(strlen('sdk_test')+1);
    strcpy(pRequest->psp_MerchantId, 'sdk_test');

    pRequest->psp_QueryCriteria = malloc(strlen('T')+1);
    strcpy(pRequest->psp_QueryCriteria, 'T');

    pRequest->psp_QueryCriteriaId = malloc(strlen('2693310')+1);
    strcpy(pRequest->psp_QueryCriteriaId, '2693310');

    pRequest->psp_PosDateTime = malloc(strlen('2019-12-01 12:00:00')+1);
    strcpy(pRequest->psp_PosDateTime, '2019-12-01 12:00:00');


    pResponse = &Response;

    showRequest(SIMPLE_QUERY_TX_TYPE,(char *)pRequest);
    sendRequest(SIMPLE_QUERY_TX_TYPE, YOUR_SECRET_KEY, (char *)pRequest, pResponse);
    showResponse(SIMPLE_QUERY_TX_TYPE,(char *)pResponse);
}
