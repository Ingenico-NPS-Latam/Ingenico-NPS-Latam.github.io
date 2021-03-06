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

    AUTHORIZE_2P_REQ_STRUCT Request, *pRequest;
    AUTHORIZE_2P_RESP_STRUCT Response, *pResponse;

    pRequest = &Request;
    memset(pRequest, 0, sizeof(AUTHORIZE_2P_REQ_STRUCT));

    pRequest->psp_Version = malloc(strlen('2.2')+1);
    strcpy(pRequest->psp_Version, '2.2');

    pRequest->psp_MerchantId = malloc(strlen('sdk_test')+1);
    strcpy(pRequest->psp_MerchantId, 'sdk_test');

    pRequest->psp_TxSource = malloc(strlen('WEB')+1);
    strcpy(pRequest->psp_TxSource, 'WEB');

    pRequest->psp_MerchTxRef = malloc(strlen('ORDERX1466Xz-3')+1);
    strcpy(pRequest->psp_MerchTxRef, 'ORDERX1466Xz-3');

    pRequest->psp_MerchOrderId = malloc(strlen('ORDERX1466Xz')+1);
    strcpy(pRequest->psp_MerchOrderId, 'ORDERX1466Xz');

    pRequest->psp_Amount = malloc(strlen('15050')+1);
    strcpy(pRequest->psp_Amount, '15050');

    pRequest->psp_NumPayments = malloc(strlen('1')+1);
    strcpy(pRequest->psp_NumPayments, '1');

    pRequest->psp_Currency = malloc(strlen('032')+1);
    strcpy(pRequest->psp_Currency, '032');

    pRequest->psp_Country = malloc(strlen('ARG')+1);
    strcpy(pRequest->psp_Country, 'ARG');

    pRequest->psp_Product = malloc(strlen('14')+1);
    strcpy(pRequest->psp_Product, '14');

    pRequest->psp_CardNumber = malloc(strlen('4507990000000010')+1);
    strcpy(pRequest->psp_CardNumber, '4507990000000010');

    pRequest->psp_CardExpDate = malloc(strlen('1912')+1);
    strcpy(pRequest->psp_CardExpDate, '1912');

    pRequest->psp_PosDateTime = malloc(strlen('2019-12-01 12:00:00')+1);
    strcpy(pRequest->psp_PosDateTime, '2019-12-01 12:00:00');

    pRequest->psp_3dSecure_XID = malloc(strlen('MjY0MjAxNjA4MDIyMDUzMzYyNjU=')+1);
    strcpy(pRequest->psp_3dSecure_XID, 'MjY0MjAxNjA4MDIyMDUzMzYyNjU=');

    pRequest->psp_3dSecure_CAVV = malloc(strlen('AAABBYZ3N5Qhl3kBU3c3ELGUsMY=')+1);
    strcpy(pRequest->psp_3dSecure_CAVV, 'AAABBYZ3N5Qhl3kBU3c3ELGUsMY=');

    pRequest->psp_3dSecure_ECI = malloc(strlen('05')+1);
    strcpy(pRequest->psp_3dSecure_ECI, '05');

    pRequest->psp_3dSecure_Secured = malloc(strlen('1')+1);
    strcpy(pRequest->psp_3dSecure_Secured, '1');

    pRequest->psp_3dSecure_ProtocolVersion = malloc(strlen('2.1.0')+1);
    strcpy(pRequest->psp_3dSecure_ProtocolVersion, '2.1.0');

    pRequest->psp_3dSecure_DirectoryServerTransactionId = malloc(strlen('c4e59ceb-a382-4d6a-bc87-385d591fa09d')+1);
    strcpy(pRequest->psp_3dSecure_DirectoryServerTransactionId, 'c4e59ceb-a382-4d6a-bc87-385d591fa09d');

    pResponse = &Response;

    showRequest(AUTHORIZE_2P_TYPE,(char *)pRequest);
    sendRequest(AUTHORIZE_2P_TYPE, YOUR_SECRET_KEY, (char *)pRequest, pResponse);
    showResponse(AUTHORIZE_2P_TYPE,(char *)pResponse);
}
