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

    UPDATE_CUSTOMER_REQ_STRUCT Request, *pRequest;
    UPDATE_CUSTOMER_RESP_STRUCT Response, *pResponse;

    pRequest = &Request;
    memset(pRequest, 0, sizeof(UPDATE_CUSTOMER_REQ_STRUCT));

    pRequest->psp_Version = malloc(strlen('2.2')+1);
    strcpy(pRequest->psp_Version, '2.2');

    pRequest->psp_MerchantId = malloc(strlen('sdk_test')+1);
    strcpy(pRequest->psp_MerchantId, 'sdk_test');

    pRequest->psp_CustomerId = malloc(strlen('bMnVPbNgX55oUz1VLgC41E5iD2rYRo2b')+1);
    strcpy(pRequest->psp_CustomerId, 'bMnVPbNgX55oUz1VLgC41E5iD2rYRo2b');

    pRequest->psp_EmailAddress = malloc(strlen('jhon.doe@example.com')+1);
    strcpy(pRequest->psp_EmailAddress, 'jhon.doe@example.com');

    pRequest->psp_AlternativeEmailAddress = malloc(strlen('jdoe@example.com')+1);
    strcpy(pRequest->psp_AlternativeEmailAddress, 'jdoe@example.com');

    pRequest->psp_AccountCreatedAt = malloc(strlen('2010-10-23')+1);
    strcpy(pRequest->psp_AccountCreatedAt, '2010-10-23');

    pRequest->psp_AccountID = malloc(strlen('jdoe78')+1);
    strcpy(pRequest->psp_AccountID, 'jdoe78');

    PAYMENT_METHOD_INPUT_DETAILS_STRUCT PaymentMethod, *PaymentMethod;
    pPaymentMethod = &PaymentMethod;
    memset(ptr, 0, sizeof(PAYMENT_METHOD_INPUT_DETAILS_STRUCT);

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

    pPaymentMethod->CardInputDetails = pCardInputDetails;

    pRequest->psp_PaymentMethod = pPaymentMethod;

    pRequest->psp_PosDateTime = malloc(strlen('2008-01-12 13:05:00')+1);
    strcpy(pRequest->psp_PosDateTime, '2008-01-12 13:05:00');


    pResponse = &Response;

    showRequest(UPDATE_CUSTOMER_TYPE,(char *)pRequest);
    sendRequest(UPDATE_CUSTOMER_TYPE, YOUR_SECRET_KEY, (char *)pRequest, pResponse);
    showResponse(UPDATE_CUSTOMER_TYPE,(char *)pResponse);
}
