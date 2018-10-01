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

    RECACHE_PAYMENT_METHOD_TOKEN_REQ_STRUCT Request, *pRequest;
    RECACHE_PAYMENT_METHOD_TOKEN_RESP_STRUCT Response, *pResponse;

    pRequest = &Request;
    memset(pRequest, 0, sizeof(RECACHE_PAYMENT_METHOD_TOKEN_REQ_STRUCT));

    pRequest->psp_Version = malloc(strlen('2.2')+1);
    strcpy(pRequest->psp_Version, '2.2');

    pRequest->psp_MerchantId = malloc(strlen('sdk_test')+1);
    strcpy(pRequest->psp_MerchantId, 'sdk_test');

    pRequest->psp_PaymentMethodId = malloc(strlen('Nzmd7DyGytXXC5PtKwnCsXXuQWHJB9EE')+1);
    strcpy(pRequest->psp_PaymentMethodId, 'Nzmd7DyGytXXC5PtKwnCsXXuQWHJB9EE');

    pRequest->psp_CardSecurityCode = malloc(strlen('123')+1);
    strcpy(pRequest->psp_CardSecurityCode, '123');

    PERSON_STRUCT Person, *Person;
    pPerson = &Person;
    memset(ptr, 0, sizeof(PERSON_STRUCT);

    pPerson->FirstName = malloc(strlen('John')+1);
    strcpy(pPerson->FirstName, 'John');

    pPerson->DateOfBirth = malloc(strlen('1979-01-12')+1);
    strcpy(pPerson->DateOfBirth, '1979-01-12');

    pPerson->LastName = malloc(strlen('Doe')+1);
    strcpy(pPerson->LastName, 'Doe');

    pPerson->MiddleName = malloc(strlen('Michael')+1);
    strcpy(pPerson->MiddleName, 'Michael');

    pPerson->PhoneNumber1 = malloc(strlen('+1 011 11111111')+1);
    strcpy(pPerson->PhoneNumber1, '+1 011 11111111');

    pPerson->PhoneNumber2 = malloc(strlen('+1 011 22222222')+1);
    strcpy(pPerson->PhoneNumber2, '+1 011 22222222');

    pPerson->Gender = malloc(strlen('M')+1);
    strcpy(pPerson->Gender, 'M');

    pPerson->Nationality = malloc(strlen('ARG')+1);
    strcpy(pPerson->Nationality, 'ARG');

    pPerson->IDNumber = malloc(strlen('54111111')+1);
    strcpy(pPerson->IDNumber, '54111111');

    pPerson->IDType = malloc(strlen('200')+1);
    strcpy(pPerson->IDType, '200');

    pRequest->psp_Person = pPerson;

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

    pRequest->psp_Address = pAddress;

    pRequest->psp_ClientSession = malloc(strlen('C5jwwbyAYneLbvZe0IYPHTvn7ODMb3vG8ZqCYaYIioUmWUbcgKscGpg8WhXrspRs')+1);
    strcpy(pRequest->psp_ClientSession, 'C5jwwbyAYneLbvZe0IYPHTvn7ODMb3vG8ZqCYaYIioUmWUbcgKscGpg8WhXrspRs');


    pResponse = &Response;

    showRequest(RECACHE_PAYMENT_METHOD_TOKEN_TYPE,(char *)pRequest);
    sendRequest(RECACHE_PAYMENT_METHOD_TOKEN_TYPE, YOUR_SECRET_KEY, (char *)pRequest, pResponse);
    showResponse(RECACHE_PAYMENT_METHOD_TOKEN_TYPE,(char *)pResponse);
}
