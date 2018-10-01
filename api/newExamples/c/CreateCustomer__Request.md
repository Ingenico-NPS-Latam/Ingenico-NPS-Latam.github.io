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

    CREATE_CUSTOMER_REQ_STRUCT Request, *pRequest;
    CREATE_CUSTOMER_RESP_STRUCT Response, *pResponse;

    pRequest = &Request;
    memset(pRequest, 0, sizeof(CREATE_CUSTOMER_REQ_STRUCT));

    pRequest->psp_Version = malloc(strlen('2.2')+1);
    strcpy(pRequest->psp_Version, '2.2');

    pRequest->psp_MerchantId = malloc(strlen('sdk_test')+1);
    strcpy(pRequest->psp_MerchantId, 'sdk_test');

    pRequest->psp_EmailAddress = malloc(strlen('jhon.doe@example.com')+1);
    strcpy(pRequest->psp_EmailAddress, 'jhon.doe@example.com');

    pRequest->psp_AlternativeEmailAddress = malloc(strlen('jdoe@example.com')+1);
    strcpy(pRequest->psp_AlternativeEmailAddress, 'jdoe@example.com');

    pRequest->psp_AccountID = malloc(strlen('jdoe78')+1);
    strcpy(pRequest->psp_AccountID, 'jdoe78');

    pRequest->psp_AccountCreatedAt = malloc(strlen('2010-10-23')+1);
    strcpy(pRequest->psp_AccountCreatedAt, '2010-10-23');

    PAYMENT_METHOD_INPUT_DETAILS_STRUCT PaymentMethod, *PaymentMethod;
    pPaymentMethod = &PaymentMethod;
    memset(ptr, 0, sizeof(PAYMENT_METHOD_INPUT_DETAILS_STRUCT);

    pPaymentMethod->PaymentMethodToken = malloc(strlen('KCVMXsbue5fUKOoAxvp1PTJ94gxv2dQM')+1);
    strcpy(pPaymentMethod->PaymentMethodToken, 'KCVMXsbue5fUKOoAxvp1PTJ94gxv2dQM');

    pRequest->psp_PaymentMethod = pPaymentMethod;

    pRequest->psp_PosDateTime = malloc(strlen('2008-01-12 13:05:00')+1);
    strcpy(pRequest->psp_PosDateTime, '2008-01-12 13:05:00');


    pResponse = &Response;

    showRequest(CREATE_CUSTOMER_TYPE,(char *)pRequest);
    sendRequest(CREATE_CUSTOMER_TYPE, YOUR_SECRET_KEY, (char *)pRequest, pResponse);
    showResponse(CREATE_CUSTOMER_TYPE,(char *)pResponse);
}
