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

    PAY_ONLINE_3P_REQ_STRUCT Request, *pRequest;
    PAY_ONLINE_3P_RESP_STRUCT Response, *pResponse;

    pRequest = &Request;
    memset(pRequest, 0, sizeof(PAY_ONLINE_3P_REQ_STRUCT));

    pRequest->psp_Version = malloc(strlen('2.2')+1);
    strcpy(pRequest->psp_Version, '2.2');

    pRequest->psp_MerchantId = malloc(strlen('sdk_test')+1);
    strcpy(pRequest->psp_MerchantId, 'sdk_test');

    pRequest->psp_TxSource = malloc(strlen('WEB')+1);
    strcpy(pRequest->psp_TxSource, 'WEB');

    pRequest->psp_MerchTxRef = malloc(strlen('ORDER66666-3')+1);
    strcpy(pRequest->psp_MerchTxRef, 'ORDER66666-3');

    pRequest->psp_MerchOrderId = malloc(strlen('ORDER66666')+1);
    strcpy(pRequest->psp_MerchOrderId, 'ORDER66666');

    pRequest->psp_ReturnURL = malloc(strlen('http://localhost/')+1);
    strcpy(pRequest->psp_ReturnURL, 'http://localhost/');

    pRequest->psp_FrmLanguage = malloc(strlen('es_AR')+1);
    strcpy(pRequest->psp_FrmLanguage, 'es_AR');

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

    VAULT_REFERENCE_3P_STRUCT VaultReference, *VaultReference;
    pVaultReference = &VaultReference;
    memset(ptr, 0, sizeof(VAULT_REFERENCE_3P_STRUCT);

    pVaultReference->CustomerId = malloc(strlen('K8sj5rBrGqPBczTR4LtuKE6g4iZMmY9f')+1);
    strcpy(pVaultReference->CustomerId, 'K8sj5rBrGqPBczTR4LtuKE6g4iZMmY9f');

    pRequest->psp_VaultReference = pVaultReference;

    pRequest->psp_PosDateTime = malloc(strlen('2019-12-01 12:00:00')+1);
    strcpy(pRequest->psp_PosDateTime, '2019-12-01 12:00:00');


    pResponse = &Response;

    showRequest(PAY_ONLINE_3P_TYPE,(char *)pRequest);
    sendRequest(PAY_ONLINE_3P_TYPE, YOUR_SECRET_KEY, (char *)pRequest, pResponse);
    showResponse(PAY_ONLINE_3P_TYPE,(char *)pResponse);
}
