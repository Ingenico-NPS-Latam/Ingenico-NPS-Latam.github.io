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

    PAY_ONLINE_2P_REQ_STRUCT Request, *pRequest;
    PAY_ONLINE_2P_RESP_STRUCT Response, *pResponse;

    pRequest = &Request;
    memset(pRequest, 0, sizeof(PAY_ONLINE_2P_REQ_STRUCT));

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

    pRequest->psp_Amount = malloc(strlen('1220000')+1);
    strcpy(pRequest->psp_Amount, '1220000');

    pRequest->psp_NumPayments = malloc(strlen('1')+1);
    strcpy(pRequest->psp_NumPayments, '1');

    pRequest->psp_Currency = malloc(strlen('858')+1);
    strcpy(pRequest->psp_Currency, '858');

    pRequest->psp_Country = malloc(strlen('URY')+1);
    strcpy(pRequest->psp_Country, 'URY');

    pRequest->psp_Product = malloc(strlen('5')+1);
    strcpy(pRequest->psp_Product, '5');

    pRequest->psp_CardNumber = malloc(strlen('5453010000083303')+1);
    strcpy(pRequest->psp_CardNumber, '5453010000083303');

    pRequest->psp_CardExpDate = malloc(strlen('1904')+1);
    strcpy(pRequest->psp_CardExpDate, '1904');

    pRequest->psp_PosDateTime = malloc(strlen('2019-12-01 12:00:00')+1);
    strcpy(pRequest->psp_PosDateTime, '2019-12-01 12:00:00');

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

    pRequest->psp_AmountAdditionalDetails = pAmountAdditionalDetails;

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


    pResponse = &Response;

    showRequest(PAY_ONLINE_2P_TYPE,(char *)pRequest);
    sendRequest(PAY_ONLINE_2P_TYPE, YOUR_SECRET_KEY, (char *)pRequest, pResponse);
    showResponse(PAY_ONLINE_2P_TYPE,(char *)pResponse);
}
