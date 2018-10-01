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

    GET_INSTALLMENTS_OPTIONS_REQ_STRUCT Request, *pRequest;
    GET_INSTALLMENTS_OPTIONS_RESP_STRUCT Response, *pResponse;

    pRequest = &Request;
    memset(pRequest, 0, sizeof(GET_INSTALLMENTS_OPTIONS_REQ_STRUCT));

    pRequest->psp_Version = malloc(strlen('2.2')+1);
    strcpy(pRequest->psp_Version, '2.2');

    pRequest->psp_MerchantId = malloc(strlen('sdk_test')+1);
    strcpy(pRequest->psp_MerchantId, 'sdk_test');

    pRequest->psp_Amount = malloc(strlen('100')+1);
    strcpy(pRequest->psp_Amount, '100');

    pRequest->psp_Product = malloc(strlen('14')+1);
    strcpy(pRequest->psp_Product, '14');

    pRequest->psp_Currency = malloc(strlen('152')+1);
    strcpy(pRequest->psp_Currency, '152');

    pRequest->psp_Country = malloc(strlen('CHL')+1);
    strcpy(pRequest->psp_Country, 'CHL');

    pRequest->psp_NumPayments = malloc(strlen('12')+1);
    strcpy(pRequest->psp_NumPayments, '12');

    pRequest->psp_PaymentMethodToken = malloc(strlen('KCVMXsbue5fUKOoAxvp1PTJ94gxv2dQM')+1);
    strcpy(pRequest->psp_PaymentMethodToken, 'KCVMXsbue5fUKOoAxvp1PTJ94gxv2dQM');

    pRequest->psp_ClientSession = malloc(strlen('C5jwwbyAYneLbvZe0IYPHTvn7ODMb3vG8ZqCYaYIioUmWUbcgKscGpg8WhXrspRs')+1);
    strcpy(pRequest->psp_ClientSession, 'C5jwwbyAYneLbvZe0IYPHTvn7ODMb3vG8ZqCYaYIioUmWUbcgKscGpg8WhXrspRs');

    pRequest->psp_PosDateTime = malloc(strlen('2017-04-04 13:35:20')+1);
    strcpy(pRequest->psp_PosDateTime, '2017-04-04 13:35:20');


    pResponse = &Response;

    showRequest(GET_INSTALLMENTS_OPTIONS_TYPE,(char *)pRequest);
    sendRequest(GET_INSTALLMENTS_OPTIONS_TYPE, YOUR_SECRET_KEY, (char *)pRequest, pResponse);
    showResponse(GET_INSTALLMENTS_OPTIONS_TYPE,(char *)pResponse);
}
