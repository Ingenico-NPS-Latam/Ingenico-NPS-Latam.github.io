$response = sdk.retrievePaymentMethodToken($params);

$response["psp_ResponseCod"];
$response["psp_ResponseMsg"];
$response["psp_MerchantId"];
$response["psp_PaymentMethodToken"];
$response["psp_Product"];

$pspWalletOutputDetails = $response["psp_WalletOutputDetails"];

$cardOutputDetails = $pspWalletOutputDetails["CardOutputDetails"];
$CardOutputDetails["ExpirationDate"];
$CardOutputDetails["ExpirationYear"];
$CardOutputDetails["ExpirationMonth"];
$CardOutputDetails["HolderName"];
$CardOutputDetails["IIN"];
$CardOutputDetails["Last4"];
$CardOutputDetails["NumberLength"];
$CardOutputDetails["MaskedNumber"];
$CardOutputDetails["MaskedNumberAlternative"];

$shippingDetails = $pspWalletOutputDetails["ShippingDetails"];
$ShippingDetails["Method"];

$primaryRecipient = $ShippingDetails["PrimaryRecipient"];
$PrimaryRecipient["FirstName"];
$PrimaryRecipient["PhoneNumber1"];

$address = $ShippingDetails["Address"];
$Address["Street"];

$houseNumber = $Address["HouseNumber"];
$Address["AdditionalInfo"];
$Address["City"];
$Address["Country"];
$Address["ZipCode"];

$pspAddress = $response["psp_Address"];
$pspAddress["Street"];
$pspAddress["AdditionalInfo"];
$pspAddress["City"];
$pspAddress["Country"];
$pspAddress["ZipCode"];
$response["psp_AlreadyUsed"];
$response["psp_CreatedAt"];
$response["psp_UpdatedAt"];
