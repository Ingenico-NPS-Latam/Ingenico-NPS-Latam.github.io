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

    RECACHE_PAYMENT_METHOD_TOKEN_REQ_STRUCT Request, *pRequest;
    RECACHE_PAYMENT_METHOD_TOKEN_RESP_STRUCT Response, *pResponse;

    pRequest = &Request;
    memset(pRequest, 0, sizeof(RECACHE_PAYMENT_METHOD_TOKEN_REQ_STRUCT));

    pRequest->psp_Version = malloc(strlen('2.2')+1);
    strcpy(pRequest->psp_Version, '2.2');

    pRequest->psp_MerchantId = malloc(strlen('sdk_test')+1);
    strcpy(pRequest->psp_MerchantId, 'sdk_test');

    pRequest->psp_PaymentMethodId = malloc(strlen('Nzmd7DyGytXXC5PtKwnCsXXuQWHJB9EE')+1);
    strcpy(pRequest->psp_PaymentMethodId, 'Nzmd7DyGytXXC5PtKwnCsXXuQWHJB9EE');

    pRequest->psp_CardSecurityCode = malloc(strlen('123')+1);
    strcpy(pRequest->psp_CardSecurityCode, '123');

    pRequest->psp_ClientSession = malloc(strlen('C5jwwbyAYneLbvZe0IYPHTvn7ODMb3vG8ZqCYaYIioUmWUbcgKscGpg8WhXrspRs')+1);
    strcpy(pRequest->psp_ClientSession, 'C5jwwbyAYneLbvZe0IYPHTvn7ODMb3vG8ZqCYaYIioUmWUbcgKscGpg8WhXrspRs');


    pResponse = &Response;

    showRequest(RECACHE_PAYMENT_METHOD_TOKEN_TYPE,(char *)pRequest);
    sendRequest(RECACHE_PAYMENT_METHOD_TOKEN_TYPE, YOUR_SECRET_KEY, (char *)pRequest, pResponse);
    showResponse(RECACHE_PAYMENT_METHOD_TOKEN_TYPE,(char *)pResponse);
}
