$response = sdk.createPaymentMethodToken($params)

$response["psp_ResponseCod"];
$response["psp_ResponseMsg"];
$response["psp_MerchantId"];
$response["psp_PaymentMethodToken"];
$response["psp_Product"];

$pspCardOutputDetails = $response["psp_CardOutputDetails"];
$pspCardOutputDetails["ExpirationDate"];
$pspCardOutputDetails["ExpirationYear"];
$pspCardOutputDetails["ExpirationMonth"];
$pspCardOutputDetails["HolderName"];
$pspCardOutputDetails["IIN"];
$pspCardOutputDetails["Last4"];
$pspCardOutputDetails["NumberLength"];
$pspCardOutputDetails["MaskedNumber"];
$pspCardOutputDetails["MaskedNumberAlternative"];
$response["psp_AlreadyUsed"];
$response["psp_CreatedAt"];
$response["psp_UpdatedAt"];
