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

    RETRIEVE_PAYMENT_METHOD_TOKEN_REQ_STRUCT Request, *pRequest;
    RETRIEVE_PAYMENT_METHOD_TOKEN_RESP_STRUCT Response, *pResponse;

    pRequest = &Request;
    memset(pRequest, 0, sizeof(RETRIEVE_PAYMENT_METHOD_TOKEN_REQ_STRUCT));

    pRequest->psp_Version = malloc(strlen('2.2')+1);
    strcpy(pRequest->psp_Version, '2.2');

    pRequest->psp_MerchantId = malloc(strlen('sdk_test')+1);
    strcpy(pRequest->psp_MerchantId, 'sdk_test');

    pRequest->psp_PaymentMethodToken = malloc(strlen('KCVMXsbue5fUKOoAxvp1PTJ94gxv2dQM')+1);
    strcpy(pRequest->psp_PaymentMethodToken, 'KCVMXsbue5fUKOoAxvp1PTJ94gxv2dQM');

    pRequest->psp_ClientSession = malloc(strlen('C5jwwbyAYneLbvZe0IYPHTvn7ODMb3vG8ZqCYaYIioUmWUbcgKscGpg8WhXrspRs')+1);
    strcpy(pRequest->psp_ClientSession, 'C5jwwbyAYneLbvZe0IYPHTvn7ODMb3vG8ZqCYaYIioUmWUbcgKscGpg8WhXrspRs');


    pResponse = &Response;

    showRequest(RETRIEVE_PAYMENT_METHOD_TOKEN_TYPE,(char *)pRequest);
    sendRequest(RETRIEVE_PAYMENT_METHOD_TOKEN_TYPE, YOUR_SECRET_KEY, (char *)pRequest, pResponse);
    showResponse(RETRIEVE_PAYMENT_METHOD_TOKEN_TYPE,(char *)pResponse);
}
