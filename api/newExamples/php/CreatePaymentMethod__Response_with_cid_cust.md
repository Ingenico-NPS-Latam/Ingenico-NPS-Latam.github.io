$response = sdk.createPaymentMethod($params);

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
$CardOutputDetails["HolderName"];
$CardOutputDetails["IIN"];
$CardOutputDetails["Last4"];
$CardOutputDetails["NumberLength"];
$CardOutputDetails["MaskedNumber"];
$CardOutputDetails["MaskedNumberAlternative"];
$pspPaymentMethod["FingerPrint"];

$person = $pspPaymentMethod["Person"];
$Person["FirstName"];
$Person["LastName"];
$Person["MiddleName"];
$Person["PhoneNumber1"];
$Person["PhoneNumber2"];
$Person["Gender"];
$Person["DateOfBirth"];
$Person["Nationality"];
$Person["IDNumber"];
$Person["IDType"];

$address = $pspPaymentMethod["Address"];
$Address["Street"];
$Address["HouseNumber"];
$Address["AdditionalInfo"];
$Address["City"];
$Address["StateProvince"];
$Address["Country"];
$Address["ZipCode"];
$pspPaymentMethod["CreatedAt"];
$pspPaymentMethod["UpdatedAt"];
$response["psp_CustomerId"];
$response["psp_PosDateTime"];
