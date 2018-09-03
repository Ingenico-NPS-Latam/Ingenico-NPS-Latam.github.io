use NpsSDK::Nps;
use warnings;
use strict;

my $response = NpsSDK::Nps::query_card_number($params);

$response->{psp_ResponseCod};
$response->{psp_ResponseMsg};
$response->{psp_MerchantId};
$response->{psp_QueryCriteria};
$response->{psp_QueryCriteriaId};
$response->{psp_PosDateTime};
$response->{psp_CardNumber};
