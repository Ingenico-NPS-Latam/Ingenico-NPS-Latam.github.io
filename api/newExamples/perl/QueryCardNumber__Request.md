use NpsPerlSDK::Nps;
use warnings;
use strict;

NpsPerlSDK::Configuration::configure( 
    environment => $constants::SANDBOX_ENV,
    secret_key => "_YOUR_SECRET_KEY_",
    sanitize => 1 
    );

my $params = {
    "psp_Version" => "1",
    "psp_MerchantId" => "sdk_test",
    "psp_QueryCriteria" => "T",
    "psp_QueryCriteriaId" => "76577",
    "psp_PosDateTime" => "2019-12-01 12:00:00",
};

my $response = NpsPerlSDK::Nps::query_card_number($params);