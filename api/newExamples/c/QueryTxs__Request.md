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

    QUERY_TXS_REQ_STRUCT Request, *pRequest;
    QUERY_TXS_RESP_STRUCT Response, *pResponse;

    pRequest = &Request;
    memset(pRequest, 0, sizeof(QUERY_TXS_REQ_STRUCT));

    pRequest->psp_Version = malloc(strlen('2.2')+1);
    strcpy(pRequest->psp_Version, '2.2');

    pRequest->psp_MerchantId = malloc(strlen('sdk_test')+1);
    strcpy(pRequest->psp_MerchantId, 'sdk_test');

    pRequest->psp_QueryCriteria = malloc(strlen('O')+1);
    strcpy(pRequest->psp_QueryCriteria, 'O');

    pRequest->psp_QueryCriteriaId = malloc(strlen('ORDER69461-3')+1);
    strcpy(pRequest->psp_QueryCriteriaId, 'ORDER69461-3');

    pRequest->psp_PosDateTime = malloc(strlen('2019-12-01 12:00:00')+1);
    strcpy(pRequest->psp_PosDateTime, '2019-12-01 12:00:00');


    pResponse = &Response;

    showRequest(QUERY_TXS_TYPE,(char *)pRequest);
    sendRequest(QUERY_TXS_TYPE, YOUR_SECRET_KEY, (char *)pRequest, pResponse);
    showResponse(QUERY_TXS_TYPE,(char *)pResponse);
}
