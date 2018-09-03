$response = sdk.deleteCustomer($params);

$response["psp_ResponseCod"];
$response["psp_ResponseMsg"];
$response["psp_MerchantId"];
$response["psp_CustomerId"];
$response["psp_EmailAddress"];
$response["psp_AlternativeEmailAddress"];
$response["psp_AccountID"];
$response["psp_AccountCreatedAt"];
$response["psp_DefaultPaymentMethodId"];

$pspPaymentMethods0 = $response["psp_PaymentMethods"][0];

$pspPaymentMethods0["PaymentMethodId"];
$pspPaymentMethods0["Product"];

$cardOutputDetails = $pspPaymentMethods0["CardOutputDetails"];
$CardOutputDetails["ExpirationDate"];
$CardOutputDetails["ExpirationYear"];
$CardOutputDetails["ExpirationMonth"];
$CardOutputDetails["HolderName"];
$CardOutputDetails["IIN"];
$CardOutputDetails["Last4"];
$CardOutputDetails["NumberLength"];
$CardOutputDetails["MaskedNumber"];
$CardOutputDetails["MaskedNumberAlternative"];
$pspPaymentMethods0["FingerPrint"];
$pspPaymentMethods0["CreatedAt"];
$pspPaymentMethods0["UpdatedAt"];


$response["psp_PosDateTime"];
