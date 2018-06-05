$response = sdk.getInstallmentsOptions($params)

$response["psp_ResponseCod"];
$response["psp_ResponseMsg"];
$response["psp_MerchantId"];
$response["psp_Amount"];
$response["psp_Product"];
$response["psp_Currency"];
$response["psp_Country"];
$response["psp_NumPayments"];

$pspInstallmentsOptions0 = $response["psp_InstallmentsOptions"][0];

$pspInstallmentsOptions0["NumPayments"];
$pspInstallmentsOptions0["InstallmentAmount"];


$response["psp_PosDateTime"];
