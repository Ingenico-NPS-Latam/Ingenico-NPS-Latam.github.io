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

    pPerson->Gender = malloc(strlen('M')+1);
    strcpy(pPerson->Gender, 'M');

    pPerson->DateOfBirth = malloc(strlen('1979-01-12')+1);
    strcpy(pPerson->DateOfBirth, '1979-01-12');

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

    pAddress->HouseNumber = malloc(strlen('1245')+1);
    strcpy(pAddress->HouseNumber, '1245');

    pAddress->AdditionalInfo = malloc(strlen('2 A')+1);
    strcpy(pAddress->AdditionalInfo, '2 A');

    pAddress->City = malloc(strlen('Miami')+1);
    strcpy(pAddress->City, 'Miami');

    pAddress->StateProvince = malloc(strlen('Florida')+1);
    strcpy(pAddress->StateProvince, 'Florida');

    pAddress->Country = malloc(strlen('USA')+1);
    strcpy(pAddress->Country, 'USA');

    pAddress->ZipCode = malloc(strlen('33140')+1);
    strcpy(pAddress->ZipCode, '33140');

    pRequest->psp_Address = pAddress;

    pRequest->psp_PosDateTime = malloc(strlen('2008-01-12 13:05:00')+1);
    strcpy(pRequest->psp_PosDateTime, '2008-01-12 13:05:00');


    pResponse = &Response;

    showRequest(UPDATE_CUSTOMER_TYPE,(char *)pRequest);
    sendRequest(UPDATE_CUSTOMER_TYPE, YOUR_SECRET_KEY, (char *)pRequest, pResponse);
    showResponse(UPDATE_CUSTOMER_TYPE,(char *)pResponse);
}
