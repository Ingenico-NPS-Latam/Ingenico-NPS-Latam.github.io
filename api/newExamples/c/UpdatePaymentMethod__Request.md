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

    UPDATE_PAYMENT_METHOD_REQ_STRUCT Request, *pRequest;
    UPDATE_PAYMENT_METHOD_RESP_STRUCT Response, *pResponse;

    pRequest = &Request;
    memset(pRequest, 0, sizeof(UPDATE_PAYMENT_METHOD_REQ_STRUCT));

    pRequest->psp_Version = malloc(strlen('2.2')+1);
    strcpy(pRequest->psp_Version, '2.2');

    pRequest->psp_MerchantId = malloc(strlen('sdk_test')+1);
    strcpy(pRequest->psp_MerchantId, 'sdk_test');

    pRequest->psp_PaymentMethodId = malloc(strlen('Nzmd7DyGytXXC5PtKwnCsXXuQWHJB9EE')+1);
    strcpy(pRequest->psp_PaymentMethodId, 'Nzmd7DyGytXXC5PtKwnCsXXuQWHJB9EE');

    pRequest->psp_PaymentMethodTag = malloc(strlen('Corporate card')+1);
    strcpy(pRequest->psp_PaymentMethodTag, 'Corporate card');

    CARD_INPUT_DETAILS_STRUCT CardInputDetails, *CardInputDetails;
    pCardInputDetails = &CardInputDetails;
    memset(ptr, 0, sizeof(CARD_INPUT_DETAILS_STRUCT);

    pCardInputDetails->ExpirationDate = malloc(strlen('2501')+1);
    strcpy(pCardInputDetails->ExpirationDate, '2501');

    pRequest->psp_CardInputDetails = pCardInputDetails;

    pRequest->psp_PosDateTime = malloc(strlen('2008-01-12 13:05:00')+1);
    strcpy(pRequest->psp_PosDateTime, '2008-01-12 13:05:00');


    pResponse = &Response;

    showRequest(UPDATE_PAYMENT_METHOD_TYPE,(char *)pRequest);
    sendRequest(UPDATE_PAYMENT_METHOD_TYPE, YOUR_SECRET_KEY, (char *)pRequest, pResponse);
    showResponse(UPDATE_PAYMENT_METHOD_TYPE,(char *)pResponse);
}
