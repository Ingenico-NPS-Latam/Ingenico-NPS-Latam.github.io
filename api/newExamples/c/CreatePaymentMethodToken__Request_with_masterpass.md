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

    WALLET_INPUT_DETAILS_STRUCT WalletInputDetails, *WalletInputDetails;
    pWalletInputDetails = &WalletInputDetails;
    memset(ptr, 0, sizeof(WALLET_INPUT_DETAILS_STRUCT);

    pWalletInputDetails->WalletTypeId = malloc(strlen('2')+1);
    strcpy(pWalletInputDetails->WalletTypeId, '2');

    pWalletInputDetails->WalletKey = malloc(strlen('d084703513e87cd1540a114cd7317e6642eca04e')+1);
    strcpy(pWalletInputDetails->WalletKey, 'd084703513e87cd1540a114cd7317e6642eca04e');

    pWalletInputDetails->MerchOrderId = malloc(strlen('1efed583-1824-436a-869f-286ebdb22ae9')+1);
    strcpy(pWalletInputDetails->MerchOrderId, '1efed583-1824-436a-869f-286ebdb22ae9');

    pRequest->psp_WalletInputDetails = pWalletInputDetails;

    pRequest->psp_ClientSession = malloc(strlen('C5jwwbyAYneLbvZe0IYPHTvn7ODMb3vG8ZqCYaYIioUmWUbcgKscGpg8WhXrspRs')+1);
    strcpy(pRequest->psp_ClientSession, 'C5jwwbyAYneLbvZe0IYPHTvn7ODMb3vG8ZqCYaYIioUmWUbcgKscGpg8WhXrspRs');


    pResponse = &Response;

    showRequest(CREATE_PAYMENT_METHOD_TOKEN_TYPE,(char *)pRequest);
    sendRequest(CREATE_PAYMENT_METHOD_TOKEN_TYPE, YOUR_SECRET_KEY, (char *)pRequest, pResponse);
    showResponse(CREATE_PAYMENT_METHOD_TOKEN_TYPE,(char *)pResponse);
}
