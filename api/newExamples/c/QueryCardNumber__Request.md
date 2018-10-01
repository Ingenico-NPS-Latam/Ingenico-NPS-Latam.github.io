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

    QUERY_CARD_NUMBER_REQ_STRUCT Request, *pRequest;
    QUERY_CARD_NUMBER_RESP_STRUCT Response, *pResponse;

    pRequest = &Request;
    memset(pRequest, 0, sizeof(QUERY_CARD_NUMBER_REQ_STRUCT));

    pRequest->psp_Version = malloc(strlen('1')+1);
    strcpy(pRequest->psp_Version, '1');

    pRequest->psp_MerchantId = malloc(strlen('sdk_test')+1);
    strcpy(pRequest->psp_MerchantId, 'sdk_test');

    pRequest->psp_QueryCriteria = malloc(strlen('T')+1);
    strcpy(pRequest->psp_QueryCriteria, 'T');

    pRequest->psp_QueryCriteriaId = malloc(strlen('76577')+1);
    strcpy(pRequest->psp_QueryCriteriaId, '76577');

    pRequest->psp_PosDateTime = malloc(strlen('2019-12-01 12:00:00')+1);
    strcpy(pRequest->psp_PosDateTime, '2019-12-01 12:00:00');


    pResponse = &Response;

    showRequest(QUERY_CARD_NUMBER_TYPE,(char *)pRequest);
    sendRequest(QUERY_CARD_NUMBER_TYPE, YOUR_SECRET_KEY, (char *)pRequest, pResponse);
    showResponse(QUERY_CARD_NUMBER_TYPE,(char *)pResponse);
}
