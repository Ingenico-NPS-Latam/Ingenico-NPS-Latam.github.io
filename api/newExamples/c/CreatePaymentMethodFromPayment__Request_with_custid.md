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

    CREATE_PAYMENT_METHOD_FROM_PAYMENT_REQ_STRUCT Request, *pRequest;
    CREATE_PAYMENT_METHOD_FROM_PAYMENT_RESP_STRUCT Response, *pResponse;

    pRequest = &Request;
    memset(pRequest, 0, sizeof(CREATE_PAYMENT_METHOD_FROM_PAYMENT_REQ_STRUCT));

    pRequest->psp_Version = malloc(strlen('2.2')+1);
    strcpy(pRequest->psp_Version, '2.2');

    pRequest->psp_MerchantId = malloc(strlen('sdk_test')+1);
    strcpy(pRequest->psp_MerchantId, 'sdk_test');

    pRequest->psp_TransactionId = malloc(strlen('65340022')+1);
    strcpy(pRequest->psp_TransactionId, '65340022');

    pRequest->psp_PaymentMethodTag = malloc(strlen('Corporate card')+1);
    strcpy(pRequest->psp_PaymentMethodTag, 'Corporate card');

    pRequest->psp_CustomerId = malloc(strlen('bMnVPbNgX55oUz1VLgC41E5iD2rYRo2b')+1);
    strcpy(pRequest->psp_CustomerId, 'bMnVPbNgX55oUz1VLgC41E5iD2rYRo2b');

    pRequest->psp_SetAsCustomerDefault = malloc(strlen('1')+1);
    strcpy(pRequest->psp_SetAsCustomerDefault, '1');

    pRequest->psp_PosDateTime = malloc(strlen('2008-01-12 13:05:00')+1);
    strcpy(pRequest->psp_PosDateTime, '2008-01-12 13:05:00');


    pResponse = &Response;

    showRequest(CREATE_PAYMENT_METHOD_FROM_PAYMENT_TYPE,(char *)pRequest);
    sendRequest(CREATE_PAYMENT_METHOD_FROM_PAYMENT_TYPE, YOUR_SECRET_KEY, (char *)pRequest, pResponse);
    showResponse(CREATE_PAYMENT_METHOD_FROM_PAYMENT_TYPE,(char *)pResponse);
}
