$response = sdk.payOnline2p($params);

$response["psp_ResponseCod"];
$response["psp_ResponseMsg"];
$response["psp_ResponseExtended"];
$response["psp_TransactionId"];
$response["psp_MerchantId"];
$response["psp_MerchTxRef"];
$response["psp_MerchOrderId"];
$response["psp_Amount"];
$response["psp_NumPayments"];
$response["psp_Currency"];
$response["psp_Country"];
$response["psp_Product"];
$response["psp_CardNumber"];
$response["psp_CardExpDate"];
$response["psp_AuthorizationCode"];
$response["psp_ClExternalMerchant"];
$response["psp_ClExternalTerminal"];
$response["psp_ClResponseCod"];
$response["psp_ClResponseMsg"];
$response["psp_PosDateTime"];
$response["psp_CreatedAt"];

$pspAmountAdditionalDetails = $response["psp_AmountAdditionalDetails"];
$pspAmountAdditionalDetails["Tip"];
$pspAmountAdditionalDetails["Discount"];

$taxes0 = $pspAmountAdditionalDetails["Taxes"][0];

$taxes0["TypeId"];
$taxes0["TypeDescription"];
$taxes0["Amount"];

$rate = $taxes0["Rate"];

$baseAmount = $taxes0["BaseAmount"];

$appliedAmount = $taxes0["AppliedAmount"];

$remarks = $taxes0["Remarks"];

$taxes1 = $pspAmountAdditionalDetails["Taxes"][1];

$taxes1["TypeId"];
$taxes1["TypeDescription"];
$taxes1["Amount"];
$taxes1["Rate"];
$taxes1["BaseAmount"];

$appliedAmount = $taxes1["AppliedAmount"];

$remarks = $taxes1["Remarks"];



$pspFraudScreeningResult = $response["psp_FraudScreeningResult"];
$pspFraudScreeningResult["ResultCode"];
$pspFraudScreeningResult["ResultDescription"];

$pspVerificationServicesResult = $response["psp_VerificationServicesResult"];
$pspVerificationServicesResult["ResultCodeCardSecurityCode"];
$pspVerificationServicesResult["ResultCodeBillingAddress"];
$pspVerificationServicesResult["ResultCodeBillingAddressZipCode"];
$pspVerificationServicesResult["ResultCodeBillingPersonIDType"];
$pspVerificationServicesResult["ResultCodeBillingPersonIDNumber"];
$pspVerificationServicesResult["ResultCodeBillingPersonDateOfBirth"];
$pspVerificationServicesResult["ResultCodeBillingPersonName"];
$pspVerificationServicesResult["ResultCodeBillingPersonPhoneNumber1"];
$pspVerificationServicesResult["ResultCodeCustomerEmailAddress"];
