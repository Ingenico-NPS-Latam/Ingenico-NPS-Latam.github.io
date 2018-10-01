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

    CREATE_PAYMENT_METHOD_REQ_STRUCT Request, *pRequest;
    CREATE_PAYMENT_METHOD_RESP_STRUCT Response, *pResponse;

    pRequest = &Request;
    memset(pRequest, 0, sizeof(CREATE_PAYMENT_METHOD_REQ_STRUCT));

    pRequest->psp_Version = malloc(strlen('2.2')+1);
    strcpy(pRequest->psp_Version, '2.2');

    pRequest->psp_MerchantId = malloc(strlen('sdk_test')+1);
    strcpy(pRequest->psp_MerchantId, 'sdk_test');

    pRequest->psp_CustomerId = malloc(strlen('bMnVPbNgX55oUz1VLgC41E5iD2rYRo2b')+1);
    strcpy(pRequest->psp_CustomerId, 'bMnVPbNgX55oUz1VLgC41E5iD2rYRo2b');

    PAYMENT_METHOD_INPUT_DETAILS_STRUCT PaymentMethod, *PaymentMethod;
    pPaymentMethod = &PaymentMethod;
    memset(ptr, 0, sizeof(PAYMENT_METHOD_INPUT_DETAILS_STRUCT);

    pPaymentMethod->PaymentMethodToken = malloc(strlen('HGIYeXKJpQyBvO3pHuZTN9JZiVPnzQaQ')+1);
    strcpy(pPaymentMethod->PaymentMethodToken, 'HGIYeXKJpQyBvO3pHuZTN9JZiVPnzQaQ');

    pPaymentMethod->PaymentMethodTag = malloc(strlen('Corporate card')+1);
    strcpy(pPaymentMethod->PaymentMethodTag, 'Corporate card');

    PERSON_STRUCT Person, *Person;
    pPerson = &Person;
    memset(ptr, 0, sizeof(PERSON_STRUCT);

    pPerson->FirstName = malloc(strlen('John')+1);
    strcpy(pPerson->FirstName, 'John');

    pPerson->LastName = malloc(strlen('Doe')+1);
    strcpy(pPerson->LastName, 'Doe');

    pPerson->MiddleName = malloc(strlen('Michael')+1);
    strcpy(pPerson->MiddleName, 'Michael');

    pPerson->PhoneNumber1 = malloc(strlen('+1 011 11111111')+1);
    strcpy(pPerson->PhoneNumber1, '+1 011 11111111');

    pPerson->PhoneNumber2 = malloc(strlen('+1 011 22222222')+1);
    strcpy(pPerson->PhoneNumber2, '+1 011 22222222');

    pPerson->DateOfBirth = malloc(strlen('1979-01-12')+1);
    strcpy(pPerson->DateOfBirth, '1979-01-12');

    pPerson->Gender = malloc(strlen('M')+1);
    strcpy(pPerson->Gender, 'M');

    pPerson->Nationality = malloc(strlen('ARG')+1);
    strcpy(pPerson->Nationality, 'ARG');

    pPerson->IDNumber = malloc(strlen('54111111')+1);
    strcpy(pPerson->IDNumber, '54111111');

    pPerson->IDType = malloc(strlen('200')+1);
    strcpy(pPerson->IDType, '200');

    pPaymentMethod->Person = pPerson;

    ADDRESS_STRUCT Address, *Address;
    pAddress = &Address;
    memset(ptr, 0, sizeof(ADDRESS_STRUCT);

    pAddress->Street = malloc(strlen('Av. Collins')+1);
    strcpy(pAddress->Street, 'Av. Collins');

    pAddress->HouseNumber = malloc(strlen('4702')+1);
    strcpy(pAddress->HouseNumber, '4702');

    pAddress->AdditionalInfo = malloc(strlen('2 A')+1);
    strcpy(pAddress->AdditionalInfo, '2 A');

    pAddress->City = malloc(strlen('Buenos Aires')+1);
    strcpy(pAddress->City, 'Buenos Aires');

    pAddress->StateProvince = malloc(strlen('CABA')+1);
    strcpy(pAddress->StateProvince, 'CABA');

    pAddress->Country = malloc(strlen('ARG')+1);
    strcpy(pAddress->Country, 'ARG');

    pAddress->ZipCode = malloc(strlen('1425')+1);
    strcpy(pAddress->ZipCode, '1425');

    pPaymentMethod->Address = pAddress;

    pRequest->psp_PaymentMethod = pPaymentMethod;

    pRequest->psp_SetAsCustomerDefault = malloc(strlen('1')+1);
    strcpy(pRequest->psp_SetAsCustomerDefault, '1');

    pRequest->psp_PosDateTime = malloc(strlen('2008-01-12 13:05:00')+1);
    strcpy(pRequest->psp_PosDateTime, '2008-01-12 13:05:00');


    pResponse = &Response;

    showRequest(CREATE_PAYMENT_METHOD_TYPE,(char *)pRequest);
    sendRequest(CREATE_PAYMENT_METHOD_TYPE, YOUR_SECRET_KEY, (char *)pRequest, pResponse);
    showResponse(CREATE_PAYMENT_METHOD_TYPE,(char *)pResponse);
}
