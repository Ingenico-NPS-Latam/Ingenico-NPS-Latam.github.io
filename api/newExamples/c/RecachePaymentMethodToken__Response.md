RECACHE_PAYMENT_METHOD_TOKEN_RESP_STRUCT Response, *pResponse;
pResponse = &Response;

printf("psp_ResponseCod: %s\n", pResponse->psp_ResponseCod);
printf("psp_ResponseMsg: %s\n", pResponse->psp_ResponseMsg);
printf("psp_MerchantId: %s\n", pResponse->psp_MerchantId);
printf("psp_PaymentMethodToken: %s\n", pResponse->psp_PaymentMethodToken);
printf("psp_Product: %s\n", pResponse->psp_Product);

CARD_OUTPUT_DETAILS_STRUCT *pCardOutputDetailsResponse;
pCardOutputDetailsResponse = pResponse->psp_CardOutputDetails;
printf("ExpirationDate: %s\n", pCardOutputDetailsResponse->ExpirationDate);
printf("ExpirationYear: %s\n", pCardOutputDetailsResponse->ExpirationYear);
printf("ExpirationMonth: %s\n", pCardOutputDetailsResponse->ExpirationMonth);
printf("HolderName: %s\n", pCardOutputDetailsResponse->HolderName);
printf("IIN: %s\n", pCardOutputDetailsResponse->IIN);
printf("Last4: %s\n", pCardOutputDetailsResponse->Last4);
printf("NumberLength: %s\n", pCardOutputDetailsResponse->NumberLength);
printf("MaskedNumber: %s\n", pCardOutputDetailsResponse->MaskedNumber);
printf("MaskedNumberAlternative: %s\n", pCardOutputDetailsResponse->MaskedNumberAlternative);

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
printf("psp_AlreadyUsed: %s\n", pResponse->psp_AlreadyUsed);
printf("psp_CreatedAt: %s\n", pResponse->psp_CreatedAt);
printf("psp_UpdatedAt: %s\n", pResponse->psp_UpdatedAt);
