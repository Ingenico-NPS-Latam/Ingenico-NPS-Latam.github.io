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

    SPLIT_AUTHORIZE_3P_REQ_STRUCT Request, *pRequest;
    SPLIT_AUTHORIZE_3P_RESP_STRUCT Response, *pResponse;

    pRequest = &Request;
    memset(pRequest, 0, sizeof(SPLIT_AUTHORIZE_3P_REQ_STRUCT));

    pRequest->psp_Version = malloc(strlen('2.2')+1);
    strcpy(pRequest->psp_Version, '2.2');

    pRequest->psp_MerchantId = malloc(strlen('sdk_test')+1);
    strcpy(pRequest->psp_MerchantId, 'sdk_test');

    pRequest->psp_TxSource = malloc(strlen('WEB')+1);
    strcpy(pRequest->psp_TxSource, 'WEB');

    pRequest->psp_MerchOrderId = malloc(strlen('ORDER66666')+1);
    strcpy(pRequest->psp_MerchOrderId, 'ORDER66666');

    pRequest->psp_ReturnURL = malloc(strlen('http://localhost/')+1);
    strcpy(pRequest->psp_ReturnURL, 'http://localhost/');

    pRequest->psp_FrmLanguage = malloc(strlen('es_AR')+1);
    strcpy(pRequest->psp_FrmLanguage, 'es_AR');

    pRequest->psp_Amount = malloc(strlen('15050')+1);
    strcpy(pRequest->psp_Amount, '15050');

    pRequest->psp_Currency = malloc(strlen('032')+1);
    strcpy(pRequest->psp_Currency, '032');

    pRequest->psp_Country = malloc(strlen('ARG')+1);
    strcpy(pRequest->psp_Country, 'ARG');

    pRequest->psp_Product = malloc(strlen('14')+1);
    strcpy(pRequest->psp_Product, '14');

    pRequest->psp_PosDateTime = malloc(strlen('2019-12-01 12:00:00')+1);
    strcpy(pRequest->psp_PosDateTime, '2019-12-01 12:00:00');

    VAULT_REFERENCE_3P_STRUCT VaultReference, *VaultReference;
    pVaultReference = &VaultReference;
    memset(ptr, 0, sizeof(VAULT_REFERENCE_3P_STRUCT);

    pVaultReference->CustomerId = malloc(strlen('K8sj5rBrGqPBczTR4LtuKE6g4iZMmY9f')+1);
    strcpy(pVaultReference->CustomerId, 'K8sj5rBrGqPBczTR4LtuKE6g4iZMmY9f');

    pRequest->psp_VaultReference = pVaultReference;

    ARRAYOF_REQUERIMIENTOSTRUCT_SPLITAUTHORIZE_3P_TRANSACTIONS *pTransactions;
    pTransactions = (ARRAYOF_REQUERIMIENTOSTRUCT_SPLITAUTHORIZE_3P_TRANSACTIONS*)malloc(sizeof(ARRAYOF_REQUERIMIENTOSTRUCT_SPLITAUTHORIZE_3P_TRANSACTIONS));
    memset(pTransactions, 0, sizeof(ARRAYOF_REQUERIMIENTOSTRUCT_SPLITAUTHORIZE_3P_TRANSACTIONS));
    pTransactions->__size=2;

    REQUERIMIENTO_STRUCT_SPLITAUTHORIZE_3P_TRANSACTIONS *ptr;
    pTransactions->__ptr=(REQUERIMIENTO_STRUCT_SPLITAUTHORIZE_3P_TRANSACTIONS *)malloc(sizeof(REQUERIMIENTO_STRUCT_SPLITAUTHORIZE_3P_TRANSACTIONS *)*2);

    for (int i = 0; i < pTransactions->__size; ++i) {
    ptr=(REQUERIMIENTO_STRUCT_SPLITAUTHORIZE_3P_TRANSACTIONS *)malloc(sizeof(REQUERIMIENTO_STRUCT_SPLITAUTHORIZE_3P_TRANSACTIONS));
    memset(ptr, 0, sizeof(REQUERIMIENTO_STRUCT_SPLITAUTHORIZE_3P_TRANSACTIONS));

    ptr->psp_MerchantId = malloc(strlen('sdk_test')+1);
    strcpy(ptr->psp_MerchantId, 'sdk_test');

    ptr->psp_MerchTxRef = malloc(strlen('ORDER66666-3')+1);
    strcpy(ptr->psp_MerchTxRef, 'ORDER66666-3');

    ptr->psp_Product = malloc(strlen('14')+1);
    strcpy(ptr->psp_Product, '14');

    ptr->psp_Amount = malloc(strlen('10000')+1);
    strcpy(ptr->psp_Amount, '10000');

    ptr->psp_NumPayments = malloc(strlen('1')+1);
    strcpy(ptr->psp_NumPayments, '1');

    ptr->psp_MerchantId = malloc(strlen('sdk_test')+1);
    strcpy(ptr->psp_MerchantId, 'sdk_test');

    ptr->psp_MerchTxRef = malloc(strlen('ORDER66666-3')+1);
    strcpy(ptr->psp_MerchTxRef, 'ORDER66666-3');

    ptr->psp_Product = malloc(strlen('14')+1);
    strcpy(ptr->psp_Product, '14');

    ptr->psp_Amount = malloc(strlen('5050')+1);
    strcpy(ptr->psp_Amount, '5050');

    ptr->psp_NumPayments = malloc(strlen('1')+1);
    strcpy(ptr->psp_NumPayments, '1');

    pTransactions->__ptr[i]=ptr;
    }

    pRequest->Transactions=pTransactions;


    pResponse = &Response;

    showRequest(SPLIT_AUTHORIZE_3P_TYPE,(char *)pRequest);
    sendRequest(SPLIT_AUTHORIZE_3P_TYPE, YOUR_SECRET_KEY, (char *)pRequest, pResponse);
    showResponse(SPLIT_AUTHORIZE_3P_TYPE,(char *)pResponse);
}
