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

    BILLING_DETAILS_STRUCT BillingDetails, *BillingDetails;
    pBillingDetails = &BillingDetails;
    memset(ptr, 0, sizeof(BILLING_DETAILS_STRUCT);

    pBillingDetails->Invoice = malloc(strlen('54877555')+1);
    strcpy(pBillingDetails->Invoice, '54877555');

    pBillingDetails->InvoiceDate = malloc(strlen('2017-10-23')+1);
    strcpy(pBillingDetails->InvoiceDate, '2017-10-23');

    pBillingDetails->InvoiceAmount = malloc(strlen('15050')+1);
    strcpy(pBillingDetails->InvoiceAmount, '15050');

    pBillingDetails->InvoiceCurrency = malloc(strlen('032')+1);
    strcpy(pBillingDetails->InvoiceCurrency, '032');

    PERSON_STRUCT Person, *Person;
    pPerson = &Person;
    memset(ptr, 0, sizeof(PERSON_STRUCT);

    pPerson->DateOfBirth = malloc(strlen('1979-01-12')+1);
    strcpy(pPerson->DateOfBirth, '1979-01-12');

    pPerson->FirstName = malloc(strlen('John')+1);
    strcpy(pPerson->FirstName, 'John');

    pPerson->Gender = malloc(strlen('M')+1);
    strcpy(pPerson->Gender, 'M');

    pPerson->IDNumber = malloc(strlen('54111111')+1);
    strcpy(pPerson->IDNumber, '54111111');

    pPerson->IDType = malloc(strlen('200')+1);
    strcpy(pPerson->IDType, '200');

    pPerson->LastName = malloc(strlen('Doe')+1);
    strcpy(pPerson->LastName, 'Doe');

    pPerson->MiddleName = malloc(strlen('Michael')+1);
    strcpy(pPerson->MiddleName, 'Michael');

    pPerson->Nationality = malloc(strlen('ARG')+1);
    strcpy(pPerson->Nationality, 'ARG');

    pPerson->PhoneNumber1 = malloc(strlen('+1 011 11111111')+1);
    strcpy(pPerson->PhoneNumber1, '+1 011 11111111');

    pPerson->PhoneNumber2 = malloc(strlen('+1 011 22222222')+1);
    strcpy(pPerson->PhoneNumber2, '+1 011 22222222');

    pBillingDetails->Person = pPerson;

    ADDRESS_STRUCT Address, *Address;
    pAddress = &Address;
    memset(ptr, 0, sizeof(ADDRESS_STRUCT);

    pAddress->AdditionalInfo = malloc(strlen('2 A')+1);
    strcpy(pAddress->AdditionalInfo, '2 A');

    pAddress->City = malloc(strlen('Miami')+1);
    strcpy(pAddress->City, 'Miami');

    pAddress->Country = malloc(strlen('USA')+1);
    strcpy(pAddress->Country, 'USA');

    pAddress->HouseNumber = malloc(strlen('1245')+1);
    strcpy(pAddress->HouseNumber, '1245');

    pAddress->StateProvince = malloc(strlen('Florida')+1);
    strcpy(pAddress->StateProvince, 'Florida');

    pAddress->Street = malloc(strlen('Av. Collins')+1);
    strcpy(pAddress->Street, 'Av. Collins');

    pAddress->ZipCode = malloc(strlen('33140')+1);
    strcpy(pAddress->ZipCode, '33140');

    pBillingDetails->Address = pAddress;

    pRequest->psp_BillingDetails = pBillingDetails;

    SHIPPING_DETAILS_STRUCT ShippingDetails, *ShippingDetails;
    pShippingDetails = &ShippingDetails;
    memset(ptr, 0, sizeof(SHIPPING_DETAILS_STRUCT);

    pShippingDetails->TrackingNumber = malloc(strlen('154DDD54DWW11')+1);
    strcpy(pShippingDetails->TrackingNumber, '154DDD54DWW11');

    pShippingDetails->Method = malloc(strlen('10')+1);
    strcpy(pShippingDetails->Method, '10');

    pShippingDetails->Carrier = malloc(strlen('200')+1);
    strcpy(pShippingDetails->Carrier, '200');

    pShippingDetails->DeliveryDate = malloc(strlen('2014-11-20')+1);
    strcpy(pShippingDetails->DeliveryDate, '2014-11-20');

    pShippingDetails->FreightAmount = malloc(strlen('15000')+1);
    strcpy(pShippingDetails->FreightAmount, '15000');

    pShippingDetails->GiftMessage = malloc(strlen('Happy Birthday!')+1);
    strcpy(pShippingDetails->GiftMessage, 'Happy Birthday!');

    pShippingDetails->GiftWrapping = malloc(strlen('1')+1);
    strcpy(pShippingDetails->GiftWrapping, '1');

    PERSON_STRUCT PrimaryRecipient, *PrimaryRecipient;
    pPrimaryRecipient = &PrimaryRecipient;
    memset(ptr, 0, sizeof(PERSON_STRUCT);

    pPrimaryRecipient->DateOfBirth = malloc(strlen('1979-01-12')+1);
    strcpy(pPrimaryRecipient->DateOfBirth, '1979-01-12');

    pPrimaryRecipient->FirstName = malloc(strlen('John')+1);
    strcpy(pPrimaryRecipient->FirstName, 'John');

    pPrimaryRecipient->Gender = malloc(strlen('M')+1);
    strcpy(pPrimaryRecipient->Gender, 'M');

    pPrimaryRecipient->IDNumber = malloc(strlen('54111111')+1);
    strcpy(pPrimaryRecipient->IDNumber, '54111111');

    pPrimaryRecipient->IDType = malloc(strlen('200')+1);
    strcpy(pPrimaryRecipient->IDType, '200');

    pPrimaryRecipient->LastName = malloc(strlen('Doe')+1);
    strcpy(pPrimaryRecipient->LastName, 'Doe');

    pPrimaryRecipient->MiddleName = malloc(strlen('Michael')+1);
    strcpy(pPrimaryRecipient->MiddleName, 'Michael');

    pPrimaryRecipient->Nationality = malloc(strlen('ARG')+1);
    strcpy(pPrimaryRecipient->Nationality, 'ARG');

    pPrimaryRecipient->PhoneNumber1 = malloc(strlen('+1 011 11111111')+1);
    strcpy(pPrimaryRecipient->PhoneNumber1, '+1 011 11111111');

    pPrimaryRecipient->PhoneNumber2 = malloc(strlen('+1 011 22222222')+1);
    strcpy(pPrimaryRecipient->PhoneNumber2, '+1 011 22222222');

    pShippingDetails->PrimaryRecipient = pPrimaryRecipient;

    PERSON_STRUCT SecondaryRecipient, *SecondaryRecipient;
    pSecondaryRecipient = &SecondaryRecipient;
    memset(ptr, 0, sizeof(PERSON_STRUCT);

    pSecondaryRecipient->DateOfBirth = malloc(strlen('1979-01-12')+1);
    strcpy(pSecondaryRecipient->DateOfBirth, '1979-01-12');

    pSecondaryRecipient->FirstName = malloc(strlen('John')+1);
    strcpy(pSecondaryRecipient->FirstName, 'John');

    pSecondaryRecipient->Gender = malloc(strlen('M')+1);
    strcpy(pSecondaryRecipient->Gender, 'M');

    pSecondaryRecipient->IDNumber = malloc(strlen('54111111')+1);
    strcpy(pSecondaryRecipient->IDNumber, '54111111');

    pSecondaryRecipient->IDType = malloc(strlen('200')+1);
    strcpy(pSecondaryRecipient->IDType, '200');

    pSecondaryRecipient->LastName = malloc(strlen('Doe')+1);
    strcpy(pSecondaryRecipient->LastName, 'Doe');

    pSecondaryRecipient->MiddleName = malloc(strlen('Michael')+1);
    strcpy(pSecondaryRecipient->MiddleName, 'Michael');

    pSecondaryRecipient->Nationality = malloc(strlen('ARG')+1);
    strcpy(pSecondaryRecipient->Nationality, 'ARG');

    pSecondaryRecipient->PhoneNumber1 = malloc(strlen('+1 011 11111111')+1);
    strcpy(pSecondaryRecipient->PhoneNumber1, '+1 011 11111111');

    pSecondaryRecipient->PhoneNumber2 = malloc(strlen('+1 011 22222222')+1);
    strcpy(pSecondaryRecipient->PhoneNumber2, '+1 011 22222222');

    pShippingDetails->SecondaryRecipient = pSecondaryRecipient;

    ADDRESS_STRUCT Address, *Address;
    pAddress = &Address;
    memset(ptr, 0, sizeof(ADDRESS_STRUCT);

    pAddress->AdditionalInfo = malloc(strlen('2 A')+1);
    strcpy(pAddress->AdditionalInfo, '2 A');

    pAddress->City = malloc(strlen('Miami')+1);
    strcpy(pAddress->City, 'Miami');

    pAddress->Country = malloc(strlen('USA')+1);
    strcpy(pAddress->Country, 'USA');

    pAddress->HouseNumber = malloc(strlen('1245')+1);
    strcpy(pAddress->HouseNumber, '1245');

    pAddress->StateProvince = malloc(strlen('Florida')+1);
    strcpy(pAddress->StateProvince, 'Florida');

    pAddress->Street = malloc(strlen('Av. Collins')+1);
    strcpy(pAddress->Street, 'Av. Collins');

    pAddress->ZipCode = malloc(strlen('33140')+1);
    strcpy(pAddress->ZipCode, '33140');

    pShippingDetails->Address = pAddress;

    pRequest->psp_ShippingDetails = pShippingDetails;


    pResponse = &Response;

    showRequest(AUTHORIZE_2P_TYPE,(char *)pRequest);
    sendRequest(AUTHORIZE_2P_TYPE, YOUR_SECRET_KEY, (char *)pRequest, pResponse);
    showResponse(AUTHORIZE_2P_TYPE,(char *)pResponse);
}
