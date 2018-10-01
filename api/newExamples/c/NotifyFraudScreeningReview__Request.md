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

    NOTIFY_FRAUD_SCREENING_REVIEW_REQ_STRUCT Request, *pRequest;
    NOTIFY_FRAUD_SCREENING_REVIEW_RESP_STRUCT Response, *pResponse;

    pRequest = &Request;
    memset(pRequest, 0, sizeof(NOTIFY_FRAUD_SCREENING_REVIEW_REQ_STRUCT));

    pRequest->psp_Version = malloc(strlen('2.2')+1);
    strcpy(pRequest->psp_Version, '2.2');

    pRequest->psp_MerchantId = malloc(strlen('sdk_test')+1);
    strcpy(pRequest->psp_MerchantId, 'sdk_test');

    pRequest->psp_Criteria = malloc(strlen('T')+1);
    strcpy(pRequest->psp_Criteria, 'T');

    pRequest->psp_CriteriaId = malloc(strlen('ORDER69461-3')+1);
    strcpy(pRequest->psp_CriteriaId, 'ORDER69461-3');

    pRequest->psp_ReviewResult = malloc(strlen('A')+1);
    strcpy(pRequest->psp_ReviewResult, 'A');

    pRequest->psp_PosDateTime = malloc(strlen('2019-12-01 12:00:00')+1);
    strcpy(pRequest->psp_PosDateTime, '2019-12-01 12:00:00');


    pResponse = &Response;

    showRequest(NOTIFY_FRAUD_SCREENING_REVIEW_TYPE,(char *)pRequest);
    sendRequest(NOTIFY_FRAUD_SCREENING_REVIEW_TYPE, YOUR_SECRET_KEY, (char *)pRequest, pResponse);
    showResponse(NOTIFY_FRAUD_SCREENING_REVIEW_TYPE,(char *)pResponse);
}
