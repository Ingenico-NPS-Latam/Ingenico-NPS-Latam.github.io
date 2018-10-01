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

    RETRIEVE_PAYMENT_METHOD_REQ_STRUCT Request, *pRequest;
    RETRIEVE_PAYMENT_METHOD_RESP_STRUCT Response, *pResponse;

    pRequest = &Request;
    memset(pRequest, 0, sizeof(RETRIEVE_PAYMENT_METHOD_REQ_STRUCT));

    pRequest->psp_Version = malloc(strlen('2.2')+1);
    strcpy(pRequest->psp_Version, '2.2');

    pRequest->psp_MerchantId = malloc(strlen('sdk_test')+1);
    strcpy(pRequest->psp_MerchantId, 'sdk_test');

    pRequest->psp_PaymentMethodId = malloc(strlen('jGW24iDaoMBzfKHViL18TmHo9sHBgW4J')+1);
    strcpy(pRequest->psp_PaymentMethodId, 'jGW24iDaoMBzfKHViL18TmHo9sHBgW4J');

    pRequest->psp_PosDateTime = malloc(strlen('2008-01-12 13:05:00')+1);
    strcpy(pRequest->psp_PosDateTime, '2008-01-12 13:05:00');


    pResponse = &Response;

    showRequest(RETRIEVE_PAYMENT_METHOD_TYPE,(char *)pRequest);
    sendRequest(RETRIEVE_PAYMENT_METHOD_TYPE, YOUR_SECRET_KEY, (char *)pRequest, pResponse);
    showResponse(RETRIEVE_PAYMENT_METHOD_TYPE,(char *)pResponse);
}
