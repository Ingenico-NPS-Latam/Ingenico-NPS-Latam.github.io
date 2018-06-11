use NpsPerlSDK::Nps;
use warnings;
use strict;

NpsPerlSDK::Configuration::configure( 
    environment => $constants::SANDBOX_ENV,
    secret_key => "_YOUR_SECRET_KEY_",
    sanitize => 1 
    );

my $params = {
    "psp_Version" => "2.2",
    "psp_MerchantId" => "sdk_test",
    "psp_Criteria" => "T",
    "psp_CriteriaId" => "ORDER69461-3",
    "psp_ReviewResult" => "D",
    "psp_PosDateTime" => "2019-12-01 12:00:00",
};

my $response = NpsPerlSDK::Nps::notify_fraud_screening_review($params);