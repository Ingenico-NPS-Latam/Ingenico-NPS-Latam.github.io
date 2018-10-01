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

    DELETE_CUSTOMER_REQ_STRUCT Request, *pRequest;
    DELETE_CUSTOMER_RESP_STRUCT Response, *pResponse;

    pRequest = &Request;
    memset(pRequest, 0, sizeof(DELETE_CUSTOMER_REQ_STRUCT));

    pRequest->psp_Version = malloc(strlen('2.2')+1);
    strcpy(pRequest->psp_Version, '2.2');

    pRequest->psp_MerchantId = malloc(strlen('sdk_test')+1);
    strcpy(pRequest->psp_MerchantId, 'sdk_test');

    pRequest->psp_CustomerId = malloc(strlen('bMnVPbNgX55oUz1VLgC41E5iD2rYRo2b')+1);
    strcpy(pRequest->psp_CustomerId, 'bMnVPbNgX55oUz1VLgC41E5iD2rYRo2b');

    pRequest->psp_PosDateTime = malloc(strlen('2008-01-12 13:05:00')+1);
    strcpy(pRequest->psp_PosDateTime, '2008-01-12 13:05:00');


    pResponse = &Response;

    showRequest(DELETE_CUSTOMER_TYPE,(char *)pRequest);
    sendRequest(DELETE_CUSTOMER_TYPE, YOUR_SECRET_KEY, (char *)pRequest, pResponse);
    showResponse(DELETE_CUSTOMER_TYPE,(char *)pResponse);
}
