CREATE_CUSTOMER_RESP_STRUCT Response, *pResponse;
pResponse = &Response;

printf("psp_ResponseCod: %s\n", pResponse->psp_ResponseCod);
printf("psp_ResponseMsg: %s\n", pResponse->psp_ResponseMsg);
printf("psp_MerchantId: %s\n", pResponse->psp_MerchantId);
printf("psp_CustomerId: %s\n", pResponse->psp_CustomerId);
printf("psp_EmailAddress: %s\n", pResponse->psp_EmailAddress);
printf("psp_AlternativeEmailAddress: %s\n", pResponse->psp_AlternativeEmailAddress);
printf("psp_AccountID: %s\n", pResponse->psp_AccountID);
printf("psp_AccountCreatedAt: %s\n", pResponse->psp_AccountCreatedAt);

PERSON_STRUCT *pPersonResponse;
pPersonResponse = pResponse->psp_Person;
printf("FirstName: %s\n", pPersonResponse->FirstName);
printf("LastName: %s\n", pPersonResponse->LastName);
printf("MiddleName: %s\n", pPersonResponse->MiddleName);
printf("PhoneNumber1: %s\n", pPersonResponse->PhoneNumber1);
printf("PhoneNumber2: %s\n", pPersonResponse->PhoneNumber2);
printf("Gender: %s\n", pPersonResponse->Gender);
printf("DateOfBirth: %s\n", pPersonResponse->DateOfBirth);
printf("Nationality: %s\n", pPersonResponse->Nationality);
printf("IDNumber: %s\n", pPersonResponse->IDNumber);
printf("IDType: %s\n", pPersonResponse->IDType);

ADDRESS_STRUCT *pAddressResponse;
pAddressResponse = pResponse->psp_Address;
printf("Street: %s\n", pAddressResponse->Street);
printf("HouseNumber: %s\n", pAddressResponse->HouseNumber);
printf("AdditionalInfo: %s\n", pAddressResponse->AdditionalInfo);
printf("City: %s\n", pAddressResponse->City);
printf("StateProvince: %s\n", pAddressResponse->StateProvince);
printf("Country: %s\n", pAddressResponse->Country);
printf("ZipCode: %s\n", pAddressResponse->ZipCode);
printf("psp_DefaultPaymentMethodId: %s\n", pResponse->psp_DefaultPaymentMethodId);

ARRAYOF_PAYMENT_METHODS_OUTPUT_DETAILS_STRUCT *pPaymentMethods;
pPaymentMethods = pResponse->psp_PaymentMethods;

for (i = 0; i < pPaymentMethods->__size; i++) {
PAYMENT_METHODS_OUTPUT_DETAILS_STRUCT *pPaymentMethods0;
pPaymentMethods0 = pPaymentMethods->__ptr[0];
printf("PaymentMethodId: %s\n", pPaymentMethods0->PaymentMethodId);
printf("Product: %s\n", pPaymentMethods0->Product);

CARD_OUTPUT_DETAILS_STRUCT *pCardOutputDetailsResponse;
pCardOutputDetailsResponse = pPaymentMethods0->CardOutputDetails;
printf("ExpirationDate: %s\n", pCardOutputDetailsResponse->ExpirationDate);
printf("ExpirationYear: %s\n", pCardOutputDetailsResponse->ExpirationYear);
printf("ExpirationMonth: %s\n", pCardOutputDetailsResponse->ExpirationMonth);
printf("HolderName: %s\n", pCardOutputDetailsResponse->HolderName);
printf("IIN: %s\n", pCardOutputDetailsResponse->IIN);
printf("Last4: %s\n", pCardOutputDetailsResponse->Last4);
printf("NumberLength: %s\n", pCardOutputDetailsResponse->NumberLength);
printf("MaskedNumber: %s\n", pCardOutputDetailsResponse->MaskedNumber);
printf("MaskedNumberAlternative: %s\n", pCardOutputDetailsResponse->MaskedNumberAlternative);
printf("FingerPrint: %s\n", pPaymentMethods0->FingerPrint);

PERSON_STRUCT *pPersonResponse;
pPersonResponse = pPaymentMethods0->Person;
printf("FirstName: %s\n", pPersonResponse->FirstName);
printf("LastName: %s\n", pPersonResponse->LastName);
printf("MiddleName: %s\n", pPersonResponse->MiddleName);
printf("PhoneNumber1: %s\n", pPersonResponse->PhoneNumber1);
printf("PhoneNumber2: %s\n", pPersonResponse->PhoneNumber2);
printf("Gender: %s\n", pPersonResponse->Gender);
printf("DateOfBirth: %s\n", pPersonResponse->DateOfBirth);
printf("Nationality: %s\n", pPersonResponse->Nationality);
printf("IDNumber: %s\n", pPersonResponse->IDNumber);
printf("IDType: %s\n", pPersonResponse->IDType);

ADDRESS_STRUCT *pAddressResponse;
pAddressResponse = pPaymentMethods0->Address;
printf("Street: %s\n", pAddressResponse->Street);
printf("HouseNumber: %s\n", pAddressResponse->HouseNumber);
printf("AdditionalInfo: %s\n", pAddressResponse->AdditionalInfo);
printf("City: %s\n", pAddressResponse->City);
printf("StateProvince: %s\n", pAddressResponse->StateProvince);
printf("Country: %s\n", pAddressResponse->Country);
printf("ZipCode: %s\n", pAddressResponse->ZipCode);
printf("CreatedAt: %s\n", pPaymentMethods0->CreatedAt);
printf("UpdatedAt: %s\n", pPaymentMethods0->UpdatedAt);

}
printf("psp_PosDateTime: %s\n", pResponse->psp_PosDateTime);
