CREATE_PAYMENT_METHOD_TOKEN_RESP_STRUCT Response, *pResponse;
pResponse = &Response;

printf("psp_ResponseCod: %s\n", pResponse->psp_ResponseCod);
printf("psp_ResponseMsg: %s\n", pResponse->psp_ResponseMsg);
printf("psp_MerchantId: %s\n", pResponse->psp_MerchantId);
printf("psp_PaymentMethodToken: %s\n", pResponse->psp_PaymentMethodToken);
printf("psp_Product: %s\n", pResponse->psp_Product);

WALLET_OUTPUT_DETAILS_STRUCT *pWalletOutputDetailsResponse;
pWalletOutputDetailsResponse = pResponse->psp_WalletOutputDetails;

CARD_OUTPUT_DETAILS_STRUCT *pCardOutputDetailsResponse;
pCardOutputDetailsResponse = pWalletOutputDetailsResponse->CardOutputDetails;
printf("ExpirationDate: %s\n", pCardOutputDetailsResponse->ExpirationDate);
printf("ExpirationYear: %s\n", pCardOutputDetailsResponse->ExpirationYear);
printf("ExpirationMonth: %s\n", pCardOutputDetailsResponse->ExpirationMonth);
printf("HolderName: %s\n", pCardOutputDetailsResponse->HolderName);
printf("IIN: %s\n", pCardOutputDetailsResponse->IIN);
printf("Last4: %s\n", pCardOutputDetailsResponse->Last4);
printf("NumberLength: %s\n", pCardOutputDetailsResponse->NumberLength);
printf("MaskedNumber: %s\n", pCardOutputDetailsResponse->MaskedNumber);
printf("MaskedNumberAlternative: %s\n", pCardOutputDetailsResponse->MaskedNumberAlternative);

SHIPPING_DETAILS_STRUCT *pShippingDetailsResponse;
pShippingDetailsResponse = pWalletOutputDetailsResponse->ShippingDetails;
printf("Method: %s\n", pShippingDetailsResponse->Method);

PRIMARY_RECIPIENT_STRUCT *pPrimaryRecipientResponse;
pPrimaryRecipientResponse = pShippingDetailsResponse->PrimaryRecipient;
printf("FirstName: %s\n", pPrimaryRecipientResponse->FirstName);
printf("PhoneNumber1: %s\n", pPrimaryRecipientResponse->PhoneNumber1);

ADDRESS_STRUCT *pAddressResponse;
pAddressResponse = pShippingDetailsResponse->Address;
printf("Street: %s\n", pAddressResponse->Street);
printf("HouseNumber: %s\n", pAddressResponse->HouseNumber);
printf("AdditionalInfo: %s\n", pAddressResponse->AdditionalInfo);
printf("City: %s\n", pAddressResponse->City);
printf("Country: %s\n", pAddressResponse->Country);
printf("ZipCode: %s\n", pAddressResponse->ZipCode);

ADDRESS_STRUCT *pAddressResponse;
pAddressResponse = pResponse->psp_Address;
printf("Street: %s\n", pAddressResponse->Street);
printf("AdditionalInfo: %s\n", pAddressResponse->AdditionalInfo);
printf("City: %s\n", pAddressResponse->City);
printf("Country: %s\n", pAddressResponse->Country);
printf("ZipCode: %s\n", pAddressResponse->ZipCode);
printf("psp_AlreadyUsed: %s\n", pResponse->psp_AlreadyUsed);
printf("psp_CreatedAt: %s\n", pResponse->psp_CreatedAt);
printf("psp_UpdatedAt: %s\n", pResponse->psp_UpdatedAt);
