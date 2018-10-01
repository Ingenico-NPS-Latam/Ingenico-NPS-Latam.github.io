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

    CREATE_PAYMENT_METHOD_TOKEN_REQ_STRUCT Request, *pRequest;
    CREATE_PAYMENT_METHOD_TOKEN_RESP_STRUCT Response, *pResponse;

    pRequest = &Request;
    memset(pRequest, 0, sizeof(CREATE_PAYMENT_METHOD_TOKEN_REQ_STRUCT));

    pRequest->psp_Version = malloc(strlen('2.2')+1);
    strcpy(pRequest->psp_Version, '2.2');

    pRequest->psp_MerchantId = malloc(strlen('sdk_test')+1);
    strcpy(pRequest->psp_MerchantId, 'sdk_test');

    CARD_INPUT_DETAILS_STRUCT CardInputDetails, *CardInputDetails;
    pCardInputDetails = &CardInputDetails;
    memset(ptr, 0, sizeof(CARD_INPUT_DETAILS_STRUCT);

    pCardInputDetails->Number = malloc(strlen('4507990000000010')+1);
    strcpy(pCardInputDetails->Number, '4507990000000010');

    pCardInputDetails->ExpirationDate = malloc(strlen('2501')+1);
    strcpy(pCardInputDetails->ExpirationDate, '2501');

    pCardInputDetails->SecurityCode = malloc(strlen('123')+1);
    strcpy(pCardInputDetails->SecurityCode, '123');

    pCardInputDetails->HolderName = malloc(strlen('JOHN DOE')+1);
    strcpy(pCardInputDetails->HolderName, 'JOHN DOE');

    pRequest->psp_CardInputDetails = pCardInputDetails;

    pRequest->psp_ClientSession = malloc(strlen('C5jwwbyAYneLbvZe0IYPHTvn7ODMb3vG8ZqCYaYIioUmWUbcgKscGpg8WhXrspRs')+1);
    strcpy(pRequest->psp_ClientSession, 'C5jwwbyAYneLbvZe0IYPHTvn7ODMb3vG8ZqCYaYIioUmWUbcgKscGpg8WhXrspRs');


    pResponse = &Response;

    showRequest(CREATE_PAYMENT_METHOD_TOKEN_TYPE,(char *)pRequest);
    sendRequest(CREATE_PAYMENT_METHOD_TOKEN_TYPE, YOUR_SECRET_KEY, (char *)pRequest, pResponse);
    showResponse(CREATE_PAYMENT_METHOD_TOKEN_TYPE,(char *)pResponse);
}
