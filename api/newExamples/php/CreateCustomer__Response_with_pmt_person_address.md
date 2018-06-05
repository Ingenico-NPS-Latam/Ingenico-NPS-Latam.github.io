$response = sdk.createCustomer($params)

$response["psp_ResponseCod"];
$response["psp_ResponseMsg"];
$response["psp_MerchantId"];
$response["psp_CustomerId"];
$response["psp_EmailAddress"];
$response["psp_AlternativeEmailAddress"];
$response["psp_AccountID"];
$response["psp_AccountCreatedAt"];

$pspPerson = $response["psp_Person"];
$pspPerson["FirstName"];
$pspPerson["LastName"];
$pspPerson["MiddleName"];
$pspPerson["PhoneNumber1"];
$pspPerson["PhoneNumber2"];
$pspPerson["Gender"];
$pspPerson["DateOfBirth"];
$pspPerson["Nationality"];
$pspPerson["IDNumber"];
$pspPerson["IDType"];

$pspAddress = $response["psp_Address"];
$pspAddress["Street"];
$pspAddress["HouseNumber"];
$pspAddress["AdditionalInfo"];
$pspAddress["City"];
$pspAddress["StateProvince"];
$pspAddress["Country"];
$pspAddress["ZipCode"];
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

$person = $pspPaymentMethods0["Person"];
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

$address = $pspPaymentMethods0["Address"];
$Address["Street"];
$Address["HouseNumber"];
$Address["AdditionalInfo"];
$Address["City"];
$Address["StateProvince"];
$Address["Country"];
$Address["ZipCode"];
$pspPaymentMethods0["CreatedAt"];
$pspPaymentMethods0["UpdatedAt"];


$response["psp_PosDateTime"];
