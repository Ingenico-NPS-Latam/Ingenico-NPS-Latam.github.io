use NpsSDK::Nps;
use warnings;
use strict;

my $response = NpsSDK::Nps::retrieve_customer($params);

$response->{psp_ResponseCod};
$response->{psp_ResponseMsg};
$response->{psp_MerchantId};
$response->{psp_CustomerId};
$response->{psp_EmailAddress};
$response->{psp_AlternativeEmailAddress};
$response->{psp_AccountID};
$response->{psp_AccountCreatedAt};
$response->{psp_PosDateTime};
