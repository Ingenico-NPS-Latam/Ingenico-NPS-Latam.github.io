use NpsSDK::Nps;
use warnings;
use strict;

my $response = NpsSDK::Nps::fraud_screening($params);

$response->{psp_ResponseCod};
$response->{psp_ResponseMsg};

my $pspResult = $response->{psp_Result};
$pspResult->{ResultCode};
$pspResult->{ResultDescription};
$response->{psp_OrderId};
$response->{psp_MerchantId};
$response->{psp_MerchTxRef};
$response->{psp_MerchOrderId};
$response->{psp_Amount};
$response->{psp_NumPayments};
$response->{psp_Currency};
$response->{psp_Country};
$response->{psp_Product};
$response->{psp_CardExpDate};
$response->{psp_PosDateTime};
$response->{psp_CreatedAt};
