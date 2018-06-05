use NpsPerlSDK::Nps;
use warnings;
use strict;

my $response = NpsSDK::Nps::change_secret_key($params);

$response->{psp_ResponseCod};
$response->{psp_ResponseMsg};
$response->{psp_MerchantId};
$response->{psp_PosDateTime};
