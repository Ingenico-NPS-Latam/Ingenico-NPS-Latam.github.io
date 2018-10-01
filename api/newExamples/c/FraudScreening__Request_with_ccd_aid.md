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

    FRAUD_SCREENING_REQ_STRUCT Request, *pRequest;
    FRAUD_SCREENING_RESP_STRUCT Response, *pResponse;

    pRequest = &Request;
    memset(pRequest, 0, sizeof(FRAUD_SCREENING_REQ_STRUCT));

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

    pRequest->psp_PosDateTime = malloc(strlen('2916-12-01 12:00:00')+1);
    strcpy(pRequest->psp_PosDateTime, '2916-12-01 12:00:00');

    CUSTOMER_ADDITIONAL_DETAILS_STRUCT CustomerAdditionalDetails, *CustomerAdditionalDetails;
    pCustomerAdditionalDetails = &CustomerAdditionalDetails;
    memset(ptr, 0, sizeof(CUSTOMER_ADDITIONAL_DETAILS_STRUCT);

    pCustomerAdditionalDetails->EmailAddress = malloc(strlen('jdoe@email.com')+1);
    strcpy(pCustomerAdditionalDetails->EmailAddress, 'jdoe@email.com');

    pCustomerAdditionalDetails->AlternativeEmailAddress = malloc(strlen('Jdoe79@email.com')+1);
    strcpy(pCustomerAdditionalDetails->AlternativeEmailAddress, 'Jdoe79@email.com');

    pCustomerAdditionalDetails->IPAddress = malloc(strlen('192.168.158.190')+1);
    strcpy(pCustomerAdditionalDetails->IPAddress, '192.168.158.190');

    pCustomerAdditionalDetails->AccountID = malloc(strlen('Jdoe78')+1);
    strcpy(pCustomerAdditionalDetails->AccountID, 'Jdoe78');

    pCustomerAdditionalDetails->AccountCreatedAt = malloc(strlen('2010-10-23')+1);
    strcpy(pCustomerAdditionalDetails->AccountCreatedAt, '2010-10-23');

    pCustomerAdditionalDetails->AccountPreviousActivity = malloc(strlen('1')+1);
    strcpy(pCustomerAdditionalDetails->AccountPreviousActivity, '1');

    pCustomerAdditionalDetails->AccountHasCredentials = malloc(strlen('1')+1);
    strcpy(pCustomerAdditionalDetails->AccountHasCredentials, '1');

    pCustomerAdditionalDetails->DeviceType = malloc(strlen('1')+1);
    strcpy(pCustomerAdditionalDetails->DeviceType, '1');

    pCustomerAdditionalDetails->DeviceFingerPrint = malloc(strlen('KJhKHKJgh7777kgh...')+1);
    strcpy(pCustomerAdditionalDetails->DeviceFingerPrint, 'KJhKHKJgh7777kgh...');

    pCustomerAdditionalDetails->BrowserLanguage = malloc(strlen('ES')+1);
    strcpy(pCustomerAdditionalDetails->BrowserLanguage, 'ES');

    pCustomerAdditionalDetails->HttpUserAgent = malloc(strlen('Mozilla/5.0 (X11; Ubuntu; Linux x86_64; rv:21.0) Gecko/20100101 Firefox/21.0')+1);
    strcpy(pCustomerAdditionalDetails->HttpUserAgent, 'Mozilla/5.0 (X11; Ubuntu; Linux x86_64; rv:21.0) Gecko/20100101 Firefox/21.0');

    pRequest->psp_CustomerAdditionalDetails = pCustomerAdditionalDetails;

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

    AIRLINE_DETAILS_STRUCT AirlineDetails, *AirlineDetails;
    pAirlineDetails = &AirlineDetails;
    memset(ptr, 0, sizeof(AIRLINE_DETAILS_STRUCT);

    pAirlineDetails->PNR = malloc(strlen('154DDD54DWW11')+1);
    strcpy(pAirlineDetails->PNR, '154DDD54DWW11');

    ARRAYOF_LEGSTRUCT *pLegs;
    pLegs = (ARRAYOF_LEGSTRUCT*)malloc(sizeof(ARRAYOF_LEGSTRUCT));
    memset(pLegs, 0, sizeof(ARRAYOF_LEGSTRUCT));
    pLegs->__size=1;

    LEG_STRUCT *ptr;
    pLegs->__ptr=(LEG_STRUCT *)malloc(sizeof(LEG_STRUCT *)*1);

    for (int i = 0; i < pLegs->__size; ++i) {
    ptr=(LEG_STRUCT *)malloc(sizeof(LEG_STRUCT));
    memset(ptr, 0, sizeof(LEG_STRUCT));

    ptr->DepartureAirport = malloc(strlen('EZE')+1);
    strcpy(ptr->DepartureAirport, 'EZE');

    ptr->DepartureDatetime = malloc(strlen('2014-05-12 13:05:00')+1);
    strcpy(ptr->DepartureDatetime, '2014-05-12 13:05:00');

    ptr->DepartureAirportTimezone = malloc(strlen('-03:00')+1);
    strcpy(ptr->DepartureAirportTimezone, '-03:00');

    ptr->ArrivalAirport = malloc(strlen('AMS')+1);
    strcpy(ptr->ArrivalAirport, 'AMS');

    ptr->CarrierCode = malloc(strlen('KL')+1);
    strcpy(ptr->CarrierCode, 'KL');

    ptr->FlightNumber = malloc(strlen('842')+1);
    strcpy(ptr->FlightNumber, '842');

    ptr->FareBasisCode = malloc(strlen('HL7LNR')+1);
    strcpy(ptr->FareBasisCode, 'HL7LNR');

    ptr->FareClassCode = malloc(strlen('FR')+1);
    strcpy(ptr->FareClassCode, 'FR');

    ptr->BaseFare = malloc(strlen('30000')+1);
    strcpy(ptr->BaseFare, '30000');

    ptr->BaseFareCurrency = malloc(strlen('032')+1);
    strcpy(ptr->BaseFareCurrency, '032');

    pLegs->__ptr[i]=ptr;
    }

    pAirlineDetails->Legs=pLegs;

    ARRAYOF_PASSENGERSTRUCT *pPassengers;
    pPassengers = (ARRAYOF_PASSENGERSTRUCT*)malloc(sizeof(ARRAYOF_PASSENGERSTRUCT));
    memset(pPassengers, 0, sizeof(ARRAYOF_PASSENGERSTRUCT));
    pPassengers->__size=1;

    PASSENGER_STRUCT *ptr;
    pPassengers->__ptr=(PASSENGER_STRUCT *)malloc(sizeof(PASSENGER_STRUCT *)*1);

    for (int i = 0; i < pPassengers->__size; ++i) {
    ptr=(PASSENGER_STRUCT *)malloc(sizeof(PASSENGER_STRUCT));
    memset(ptr, 0, sizeof(PASSENGER_STRUCT));

    ptr->FirstName = malloc(strlen('John')+1);
    strcpy(ptr->FirstName, 'John');

    ptr->LastName = malloc(strlen('Doe')+1);
    strcpy(ptr->LastName, 'Doe');

    ptr->MiddleName = malloc(strlen('Michael')+1);
    strcpy(ptr->MiddleName, 'Michael');

    ptr->Type = malloc(strlen('A')+1);
    strcpy(ptr->Type, 'A');

    ptr->DateOfBirth = malloc(strlen('1979-01-12')+1);
    strcpy(ptr->DateOfBirth, '1979-01-12');

    ptr->Nationality = malloc(strlen('ARG')+1);
    strcpy(ptr->Nationality, 'ARG');

    ptr->IDNumber = malloc(strlen('54111111')+1);
    strcpy(ptr->IDNumber, '54111111');

    ptr->IDType = malloc(strlen('100')+1);
    strcpy(ptr->IDType, '100');

    ptr->IDCountry = malloc(strlen('ARG')+1);
    strcpy(ptr->IDCountry, 'ARG');

    ptr->LoyaltyNumber = malloc(strlen('254587547')+1);
    strcpy(ptr->LoyaltyNumber, '254587547');

    ptr->LoyaltyTier = malloc(strlen('1')+1);
    strcpy(ptr->LoyaltyTier, '1');

    pPassengers->__ptr[i]=ptr;
    }

    pAirlineDetails->Passengers=pPassengers;

    AIRLINE_TICKET_STRUCT Ticket, *Ticket;
    pTicket = &Ticket;
    memset(ptr, 0, sizeof(AIRLINE_TICKET_STRUCT);

    pTicket->TicketNumber = malloc(strlen('07411865255578')+1);
    strcpy(pTicket->TicketNumber, '07411865255578');

    pTicket->Eticket = malloc(strlen('1')+1);
    strcpy(pTicket->Eticket, '1');

    pTicket->Restricted = malloc(strlen('1')+1);
    strcpy(pTicket->Restricted, '1');

    AIRLINE_TICKET_ISSUE_STRUCT Issue, *Issue;
    pIssue = &Issue;
    memset(ptr, 0, sizeof(AIRLINE_TICKET_ISSUE_STRUCT);

    pIssue->TravelAgentCode = malloc(strlen('32165464')+1);
    strcpy(pIssue->TravelAgentCode, '32165464');

    pIssue->TravelAgentName = malloc(strlen('Washington Hilton')+1);
    strcpy(pIssue->TravelAgentName, 'Washington Hilton');

    pIssue->Date = malloc(strlen('2017-01-10')+1);
    strcpy(pIssue->Date, '2017-01-10');

    pIssue->Country = malloc(strlen('ARG')+1);
    strcpy(pIssue->Country, 'ARG');

    pIssue->City = malloc(strlen('Buenos Aires')+1);
    strcpy(pIssue->City, 'Buenos Aires');

    pIssue->Address = malloc(strlen('Av. Rivadavia 1111')+1);
    strcpy(pIssue->Address, 'Av. Rivadavia 1111');

    pTicket->Issue = pIssue;

    pTicket->TotalFareAmount = malloc(strlen('80000')+1);
    strcpy(pTicket->TotalFareAmount, '80000');

    pTicket->TotalTaxAmount = malloc(strlen('25200')+1);
    strcpy(pTicket->TotalTaxAmount, '25200');

    pTicket->TotalFeeAmount = malloc(strlen('14800')+1);
    strcpy(pTicket->TotalFeeAmount, '14800');

    pAirlineDetails->Ticket = pTicket;

    pRequest->psp_AirlineDetails = pAirlineDetails;


    pResponse = &Response;

    showRequest(FRAUD_SCREENING_TYPE,(char *)pRequest);
    sendRequest(FRAUD_SCREENING_TYPE, YOUR_SECRET_KEY, (char *)pRequest, pResponse);
    showResponse(FRAUD_SCREENING_TYPE,(char *)pResponse);
}
