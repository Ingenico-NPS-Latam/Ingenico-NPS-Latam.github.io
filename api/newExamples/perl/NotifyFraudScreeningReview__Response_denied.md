use NpsPerlSDK::Nps;
use warnings;
use strict;

my $response = NpsSDK::Nps::notify_fraud_screening_review($params);

$response->{psp_ResponseCod};
$response->{psp_ResponseMsg};
$response->{psp_MerchantId};
$response->{psp_PosDateTime};
