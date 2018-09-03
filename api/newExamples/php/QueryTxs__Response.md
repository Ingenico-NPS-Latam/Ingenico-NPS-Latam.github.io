$response = sdk.queryTxs($params);

$response["psp_ResponseCod"];
$response["psp_ResponseMsg"];
$response["psp_MerchantId"];
$response["psp_QueryCriteria"];
$response["psp_QueryCriteriaId"];
$response["psp_PosDateTime"];

$pspTransactions0 = $response["psp_Transactions"][0];

$pspTransactions0["psp_ResponseCod"];
$pspTransactions0["psp_ResponseMsg"];
$pspTransactions0["psp_ResponseExtended"];
$pspTransactions0["psp_TransactionId"];
$pspTransactions0["psp_MerchantId"];
$pspTransactions0["psp_TxSource"];
$pspTransactions0["psp_Operation"];
$pspTransactions0["psp_MerchTxRef"];
$pspTransactions0["psp_MerchOrderId"];
$pspTransactions0["psp_Amount"];
$pspTransactions0["psp_NumPayments"];
$pspTransactions0["psp_Currency"];
$pspTransactions0["psp_Country"];
$pspTransactions0["psp_Product"];
$pspTransactions0["psp_AuthorizationCode"];
$pspTransactions0["psp_BatchNro"];
$pspTransactions0["psp_TicketNumber"];
$pspTransactions0["psp_CardNumber_FSD"];
$pspTransactions0["psp_CardNumber_LFD"];
$pspTransactions0["psp_CardMask"];
$pspTransactions0["psp_ClExternalMerchant"];
$pspTransactions0["psp_ClExternalTerminal"];
$pspTransactions0["psp_ClResponseCod"];
$pspTransactions0["psp_ClResponseMsg"];
$pspTransactions0["psp_PosDateTime"];
$pspTransactions0["psp_CreatedAt"];

$pspFraudScreeningResult = $pspTransactions0["psp_FraudScreeningResult"];
$pspFraudScreeningResult["ResultCode"];
$pspFraudScreeningResult["ResultDescription"];

$pspVerificationServicesResult = $pspTransactions0["psp_VerificationServicesResult"];
$pspVerificationServicesResult["ResultCodeCardSecurityCode"];
$pspVerificationServicesResult["ResultCodeBillingAddress"];
$pspVerificationServicesResult["ResultCodeBillingAddressZipCode"];
$pspVerificationServicesResult["ResultCodeBillingPersonIDType"];
$pspVerificationServicesResult["ResultCodeBillingPersonIDNumber"];
$pspVerificationServicesResult["ResultCodeBillingPersonDateOfBirth"];
$pspVerificationServicesResult["ResultCodeBillingPersonName"];
$pspVerificationServicesResult["ResultCodeBillingPersonPhoneNumber1"];
$pspVerificationServicesResult["ResultCodeCustomerEmailAddress"];

$pspTransactions1 = $response["psp_Transactions"][1];

$pspTransactions1["psp_ResponseCod"];
$pspTransactions1["psp_ResponseMsg"];
$pspTransactions1["psp_ResponseExtended"];
$pspTransactions1["psp_TransactionId"];
$pspTransactions1["psp_MerchantId"];
$pspTransactions1["psp_TxSource"];
$pspTransactions1["psp_Operation"];
$pspTransactions1["psp_MerchTxRef"];
$pspTransactions1["psp_MerchOrderId"];
$pspTransactions1["psp_Amount"];
$pspTransactions1["psp_NumPayments"];
$pspTransactions1["psp_Currency"];
$pspTransactions1["psp_Country"];
$pspTransactions1["psp_Product"];
$pspTransactions1["psp_AuthorizationCode"];
$pspTransactions1["psp_BatchNro"];
$pspTransactions1["psp_TicketNumber"];
$pspTransactions1["psp_CardNumber_FSD"];
$pspTransactions1["psp_CardNumber_LFD"];
$pspTransactions1["psp_CardMask"];
$pspTransactions1["psp_ClExternalMerchant"];
$pspTransactions1["psp_ClExternalTerminal"];
$pspTransactions1["psp_ClResponseCod"];
$pspTransactions1["psp_ClResponseMsg"];
$pspTransactions1["psp_PosDateTime"];
$pspTransactions1["psp_CreatedAt"];

$pspFraudScreeningResult = $pspTransactions1["psp_FraudScreeningResult"];
$pspFraudScreeningResult["ResultCode"];
$pspFraudScreeningResult["ResultDescription"];

$pspVerificationServicesResult = $pspTransactions1["psp_VerificationServicesResult"];
$pspVerificationServicesResult["ResultCodeCardSecurityCode"];
$pspVerificationServicesResult["ResultCodeBillingAddress"];
$pspVerificationServicesResult["ResultCodeBillingAddressZipCode"];
$pspVerificationServicesResult["ResultCodeBillingPersonIDType"];
$pspVerificationServicesResult["ResultCodeBillingPersonIDNumber"];
$pspVerificationServicesResult["ResultCodeBillingPersonDateOfBirth"];
$pspVerificationServicesResult["ResultCodeBillingPersonName"];
$pspVerificationServicesResult["ResultCodeBillingPersonPhoneNumber1"];
$pspVerificationServicesResult["ResultCodeCustomerEmailAddress"];


