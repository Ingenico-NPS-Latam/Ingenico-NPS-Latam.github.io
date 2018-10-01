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

    pRequest->psp_Amount = malloc(strlen('2440000')+1);
    strcpy(pRequest->psp_Amount, '2440000');

    pRequest->psp_Currency = malloc(strlen('858')+1);
    strcpy(pRequest->psp_Currency, '858');

    pRequest->psp_Country = malloc(strlen('URY')+1);
    strcpy(pRequest->psp_Country, 'URY');

    pRequest->psp_Product = malloc(strlen('5')+1);
    strcpy(pRequest->psp_Product, '5');

    pRequest->psp_PosDateTime = malloc(strlen('2019-12-01 12:00:00')+1);
    strcpy(pRequest->psp_PosDateTime, '2019-12-01 12:00:00');

    BILLING_DETAILS_STRUCT BillingDetails, *BillingDetails;
    pBillingDetails = &BillingDetails;
    memset(ptr, 0, sizeof(BILLING_DETAILS_STRUCT);

    pBillingDetails->Invoice = malloc(strlen('A00024144')+1);
    strcpy(pBillingDetails->Invoice, 'A00024144');

    pBillingDetails->InvoiceAmount = malloc(strlen('1600000')+1);
    strcpy(pBillingDetails->InvoiceAmount, '1600000');

    pBillingDetails->InvoiceCurrency = malloc(strlen('858')+1);
    strcpy(pBillingDetails->InvoiceCurrency, '858');

    pRequest->psp_BillingDetails = pBillingDetails;

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

    ptr->psp_Product = malloc(strlen('5')+1);
    strcpy(ptr->psp_Product, '5');

    ptr->psp_Amount = malloc(strlen('1220000')+1);
    strcpy(ptr->psp_Amount, '1220000');

    ptr->psp_NumPayments = malloc(strlen('1')+1);
    strcpy(ptr->psp_NumPayments, '1');

    AMOUNT_ADDITIONAL_DETAILS_REQUEST_STRUCT AmountAdditionalDetails, *AmountAdditionalDetails;
    pAmountAdditionalDetails = &AmountAdditionalDetails;
    memset(ptr, 0, sizeof(AMOUNT_ADDITIONAL_DETAILS_REQUEST_STRUCT);

    pAmountAdditionalDetails->Tip = malloc(strlen('20')+1);
    strcpy(pAmountAdditionalDetails->Tip, '20');

    pAmountAdditionalDetails->Discount = malloc(strlen('1')+1);
    strcpy(pAmountAdditionalDetails->Discount, '1');

    ARRAYOF_TAXESREQUESTSTRUCT *pTaxes;
    pTaxes = (ARRAYOF_TAXESREQUESTSTRUCT*)malloc(sizeof(ARRAYOF_TAXESREQUESTSTRUCT));
    memset(pTaxes, 0, sizeof(ARRAYOF_TAXESREQUESTSTRUCT));
    pTaxes->__size=1;

    TAXES_REQUEST_STRUCT *ptr;
    pTaxes->__ptr=(TAXES_REQUEST_STRUCT *)malloc(sizeof(TAXES_REQUEST_STRUCT *)*1);

    for (int i = 0; i < pTaxes->__size; ++i) {
    ptr=(TAXES_REQUEST_STRUCT *)malloc(sizeof(TAXES_REQUEST_STRUCT));
    memset(ptr, 0, sizeof(TAXES_REQUEST_STRUCT));

    ptr->TypeId = malloc(strlen('601')+1);
    strcpy(ptr->TypeId, '601');

    ptr->Amount = malloc(strlen('220000')+1);
    strcpy(ptr->Amount, '220000');

    ptr->Rate = malloc(strlen('2200')+1);
    strcpy(ptr->Rate, '2200');

    ptr->BaseAmount = malloc(strlen('1000000')+1);
    strcpy(ptr->BaseAmount, '1000000');

    pTaxes->__ptr[i]=ptr;
    }

    pAmountAdditionalDetails->Taxes=pTaxes;

    ptr->psp_AmountAdditionalDetails = pAmountAdditionalDetails;

    ptr->psp_MerchantId = malloc(strlen('sdk_test')+1);
    strcpy(ptr->psp_MerchantId, 'sdk_test');

    ptr->psp_MerchTxRef = malloc(strlen('ORDER66666-3')+1);
    strcpy(ptr->psp_MerchTxRef, 'ORDER66666-3');

    ptr->psp_Product = malloc(strlen('5')+1);
    strcpy(ptr->psp_Product, '5');

    ptr->psp_Amount = malloc(strlen('1220000')+1);
    strcpy(ptr->psp_Amount, '1220000');

    ptr->psp_NumPayments = malloc(strlen('1')+1);
    strcpy(ptr->psp_NumPayments, '1');

    AMOUNT_ADDITIONAL_DETAILS_REQUEST_STRUCT AmountAdditionalDetails, *AmountAdditionalDetails;
    pAmountAdditionalDetails = &AmountAdditionalDetails;
    memset(ptr, 0, sizeof(AMOUNT_ADDITIONAL_DETAILS_REQUEST_STRUCT);

    pAmountAdditionalDetails->Tip = malloc(strlen('20')+1);
    strcpy(pAmountAdditionalDetails->Tip, '20');

    pAmountAdditionalDetails->Discount = malloc(strlen('1')+1);
    strcpy(pAmountAdditionalDetails->Discount, '1');

    ARRAYOF_TAXESREQUESTSTRUCT *pTaxes;
    pTaxes = (ARRAYOF_TAXESREQUESTSTRUCT*)malloc(sizeof(ARRAYOF_TAXESREQUESTSTRUCT));
    memset(pTaxes, 0, sizeof(ARRAYOF_TAXESREQUESTSTRUCT));
    pTaxes->__size=1;

    TAXES_REQUEST_STRUCT *ptr;
    pTaxes->__ptr=(TAXES_REQUEST_STRUCT *)malloc(sizeof(TAXES_REQUEST_STRUCT *)*1);

    for (int i = 0; i < pTaxes->__size; ++i) {
    ptr=(TAXES_REQUEST_STRUCT *)malloc(sizeof(TAXES_REQUEST_STRUCT));
    memset(ptr, 0, sizeof(TAXES_REQUEST_STRUCT));

    ptr->TypeId = malloc(strlen('601')+1);
    strcpy(ptr->TypeId, '601');

    ptr->Amount = malloc(strlen('220000')+1);
    strcpy(ptr->Amount, '220000');

    ptr->Rate = malloc(strlen('2200')+1);
    strcpy(ptr->Rate, '2200');

    ptr->BaseAmount = malloc(strlen('1000000')+1);
    strcpy(ptr->BaseAmount, '1000000');

    pTaxes->__ptr[i]=ptr;
    }

    pAmountAdditionalDetails->Taxes=pTaxes;

    ptr->psp_AmountAdditionalDetails = pAmountAdditionalDetails;

    pTransactions->__ptr[i]=ptr;
    }

    pRequest->Transactions=pTransactions;


    pResponse = &Response;

    showRequest(SPLIT_AUTHORIZE_3P_TYPE,(char *)pRequest);
    sendRequest(SPLIT_AUTHORIZE_3P_TYPE, YOUR_SECRET_KEY, (char *)pRequest, pResponse);
    showResponse(SPLIT_AUTHORIZE_3P_TYPE,(char *)pResponse);
}
