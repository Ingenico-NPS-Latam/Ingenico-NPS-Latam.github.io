use NpsSDK::Nps;
use warnings;
use strict;

my $response = NpsSDK::Nps::bank_payment_3p($params);

$response->{psp_ResponseCod};
$response->{psp_ResponseMsg};
$response->{psp_TransactionId};
$response->{psp_Session3p};
$response->{psp_FrontPSP_URL};
$response->{psp_MerchantId};
$response->{psp_MerchTxRef};
$response->{psp_MerchOrderId};
$response->{psp_Currency};
$response->{psp_Country};
$response->{psp_Product};
$response->{psp_PosDateTime};
$response->{psp_CreatedAt};
