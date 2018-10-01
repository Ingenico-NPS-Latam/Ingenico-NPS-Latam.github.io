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

    GET_I_I_N_DETAILS_REQ_STRUCT Request, *pRequest;
    GET_I_I_N_DETAILS_RESP_STRUCT Response, *pResponse;

    pRequest = &Request;
    memset(pRequest, 0, sizeof(GET_I_I_N_DETAILS_REQ_STRUCT));

    pRequest->psp_Version = malloc(strlen('2.2')+1);
    strcpy(pRequest->psp_Version, '2.2');

    pRequest->psp_MerchantId = malloc(strlen('sdk_test')+1);
    strcpy(pRequest->psp_MerchantId, 'sdk_test');

    pRequest->psp_IIN = malloc(strlen('424242')+1);
    strcpy(pRequest->psp_IIN, '424242');

    pRequest->psp_PosDateTime = malloc(strlen('2019-12-01 12:00:00')+1);
    strcpy(pRequest->psp_PosDateTime, '2019-12-01 12:00:00');


    pResponse = &Response;

    showRequest(GET_I_I_N_DETAILS_TYPE,(char *)pRequest);
    sendRequest(GET_I_I_N_DETAILS_TYPE, YOUR_SECRET_KEY, (char *)pRequest, pResponse);
    showResponse(GET_I_I_N_DETAILS_TYPE,(char *)pResponse);
}
