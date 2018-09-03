use NpsSDK::Nps;
use warnings;
use strict;

my $response = NpsSDK::Nps::get_iin_details($params);

$response->{psp_ResponseCod};
$response->{psp_ResponseMsg};
$response->{psp_MerchantId};
$response->{psp_Product};
$response->{psp_PosDateTime};
