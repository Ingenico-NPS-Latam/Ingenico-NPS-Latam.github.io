$response = sdk.createPaymentMethodFromPayment($params)

$response["psp_ResponseCod"];
$response["psp_ResponseMsg"];
$response["psp_MerchantId"];

$pspPaymentMethod = $response["psp_PaymentMethod"];
$pspPaymentMethod["PaymentMethodId"];
$pspPaymentMethod["PaymentMethodTag"];
$pspPaymentMethod["Product"];

$cardOutputDetails = $pspPaymentMethod["CardOutputDetails"];
$CardOutputDetails["ExpirationDate"];
$CardOutputDetails["ExpirationYear"];
$CardOutputDetails["ExpirationMonth"];
$CardOutputDetails["IIN"];
$CardOutputDetails["Last4"];
$CardOutputDetails["NumberLength"];
$CardOutputDetails["MaskedNumber"];
$CardOutputDetails["MaskedNumberAlternative"];
$pspPaymentMethod["FingerPrint"];
$pspPaymentMethod["CreatedAt"];
$pspPaymentMethod["UpdatedAt"];
$response["psp_CustomerId"];
$response["psp_PosDateTime"];
