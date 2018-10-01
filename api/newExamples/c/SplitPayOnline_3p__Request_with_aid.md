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

    SPLIT_PAY_ONLINE_3P_REQ_STRUCT Request, *pRequest;
    SPLIT_PAY_ONLINE_3P_RESP_STRUCT Response, *pResponse;

    pRequest = &Request;
    memset(pRequest, 0, sizeof(SPLIT_PAY_ONLINE_3P_REQ_STRUCT));

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

    ARRAYOF_REQUERIMIENTOSTRUCT_SPLITPAYONLINE_3P_TRANSACTIONS *pTransactions;
    pTransactions = (ARRAYOF_REQUERIMIENTOSTRUCT_SPLITPAYONLINE_3P_TRANSACTIONS*)malloc(sizeof(ARRAYOF_REQUERIMIENTOSTRUCT_SPLITPAYONLINE_3P_TRANSACTIONS));
    memset(pTransactions, 0, sizeof(ARRAYOF_REQUERIMIENTOSTRUCT_SPLITPAYONLINE_3P_TRANSACTIONS));
    pTransactions->__size=2;

    REQUERIMIENTO_STRUCT_SPLITPAYONLINE_3P_TRANSACTIONS *ptr;
    pTransactions->__ptr=(REQUERIMIENTO_STRUCT_SPLITPAYONLINE_3P_TRANSACTIONS *)malloc(sizeof(REQUERIMIENTO_STRUCT_SPLITPAYONLINE_3P_TRANSACTIONS *)*2);

    for (int i = 0; i < pTransactions->__size; ++i) {
    ptr=(REQUERIMIENTO_STRUCT_SPLITPAYONLINE_3P_TRANSACTIONS *)malloc(sizeof(REQUERIMIENTO_STRUCT_SPLITPAYONLINE_3P_TRANSACTIONS));
    memset(ptr, 0, sizeof(REQUERIMIENTO_STRUCT_SPLITPAYONLINE_3P_TRANSACTIONS));

    ptr->psp_MerchantId = malloc(strlen('sdk_test')+1);
    strcpy(ptr->psp_MerchantId, 'sdk_test');

    ptr->psp_MerchTxRef = malloc(strlen('ORDER66666-10')+1);
    strcpy(ptr->psp_MerchTxRef, 'ORDER66666-10');

    ptr->psp_Product = malloc(strlen('14')+1);
    strcpy(ptr->psp_Product, '14');

    ptr->psp_Amount = malloc(strlen('10000')+1);
    strcpy(ptr->psp_Amount, '10000');

    ptr->psp_NumPayments = malloc(strlen('1')+1);
    strcpy(ptr->psp_NumPayments, '1');

    ptr->psp_MerchantId = malloc(strlen('sdk_test')+1);
    strcpy(ptr->psp_MerchantId, 'sdk_test');

    ptr->psp_MerchTxRef = malloc(strlen('ORDER66666-11')+1);
    strcpy(ptr->psp_MerchTxRef, 'ORDER66666-11');

    ptr->psp_Product = malloc(strlen('14')+1);
    strcpy(ptr->psp_Product, '14');

    ptr->psp_Amount = malloc(strlen('5050')+1);
    strcpy(ptr->psp_Amount, '5050');

    ptr->psp_NumPayments = malloc(strlen('1')+1);
    strcpy(ptr->psp_NumPayments, '1');

    pTransactions->__ptr[i]=ptr;
    }

    pRequest->Transactions=pTransactions;

    AIRLINE_DETAILS_STRUCT AirlineDetails, *AirlineDetails;
    pAirlineDetails = &AirlineDetails;
    memset(ptr, 0, sizeof(AIRLINE_DETAILS_STRUCT);

    pAirlineDetails->PNR = malloc(strlen('154DDD54DWW11')+1);
    strcpy(pAirlineDetails->PNR, '154DDD54DWW11');

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

    showRequest(SPLIT_PAY_ONLINE_3P_TYPE,(char *)pRequest);
    sendRequest(SPLIT_PAY_ONLINE_3P_TYPE, YOUR_SECRET_KEY, (char *)pRequest, pResponse);
    showResponse(SPLIT_PAY_ONLINE_3P_TYPE,(char *)pResponse);
}
