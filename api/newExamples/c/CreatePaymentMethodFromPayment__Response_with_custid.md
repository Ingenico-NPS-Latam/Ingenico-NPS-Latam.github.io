CREATE_PAYMENT_METHOD_FROM_PAYMENT_RESP_STRUCT Response, *pResponse;
pResponse = &Response;

printf("psp_ResponseCod: %s\n", pResponse->psp_ResponseCod);
printf("psp_ResponseMsg: %s\n", pResponse->psp_ResponseMsg);
printf("psp_MerchantId: %s\n", pResponse->psp_MerchantId);

PAYMENT_METHOD_OUTPUT_DETAILS_STRUCT *pPaymentMethodResponse;
pPaymentMethodResponse = pResponse->psp_PaymentMethod;
printf("PaymentMethodId: %s\n", pPaymentMethodResponse->PaymentMethodId);
printf("PaymentMethodTag: %s\n", pPaymentMethodResponse->PaymentMethodTag);
printf("Product: %s\n", pPaymentMethodResponse->Product);

CARD_OUTPUT_DETAILS_STRUCT *pCardOutputDetailsResponse;
pCardOutputDetailsResponse = pPaymentMethodResponse->CardOutputDetails;
printf("ExpirationDate: %s\n", pCardOutputDetailsResponse->ExpirationDate);
printf("ExpirationYear: %s\n", pCardOutputDetailsResponse->ExpirationYear);
printf("ExpirationMonth: %s\n", pCardOutputDetailsResponse->ExpirationMonth);
printf("IIN: %s\n", pCardOutputDetailsResponse->IIN);
printf("Last4: %s\n", pCardOutputDetailsResponse->Last4);
printf("NumberLength: %s\n", pCardOutputDetailsResponse->NumberLength);
printf("MaskedNumber: %s\n", pCardOutputDetailsResponse->MaskedNumber);
printf("MaskedNumberAlternative: %s\n", pCardOutputDetailsResponse->MaskedNumberAlternative);
printf("FingerPrint: %s\n", pPaymentMethodResponse->FingerPrint);
printf("CreatedAt: %s\n", pPaymentMethodResponse->CreatedAt);
printf("UpdatedAt: %s\n", pPaymentMethodResponse->UpdatedAt);
printf("psp_CustomerId: %s\n", pResponse->psp_CustomerId);
printf("psp_PosDateTime: %s\n", pResponse->psp_PosDateTime);
