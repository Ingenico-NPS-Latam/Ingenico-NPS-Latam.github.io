$response = sdk.queryCardDetails($params)

$response["psp_ResponseCod"];
$response["psp_ResponseMsg"];
$response["psp_MerchantId"];
$response["psp_QueryCriteria"];
$response["psp_QueryCriteriaId"];
$response["psp_PosDateTime"];

$pspCardOutputDetails = $response["psp_CardOutputDetails"];
$pspCardOutputDetails["Number"];
$pspCardOutputDetails["ExpirationDate"];
$pspCardOutputDetails["ExpirationYear"];
$pspCardOutputDetails["ExpirationMonth"];
$pspCardOutputDetails["HolderName"];
$pspCardOutputDetails["IIN"];
$pspCardOutputDetails["Last4"];
$pspCardOutputDetails["NumberLength"];
$pspCardOutputDetails["MaskedNumber"];
$pspCardOutputDetails["MaskedNumberAlternative"];

