use NpsSDK::Nps;
use warnings;
use strict;

NpsSDK::Configuration::configure( 
    environment => $NpsSDK::Constants::SANDBOX_ENV,
    secret_key => "_YOUR_SECRET_KEY_",
    sanitize => 1 
    );

my $params = {
    "psp_Version" => "2.2",
    "psp_MerchantId" => "sdk_test",
    "psp_Criteria" => "T",
    "psp_CriteriaId" => "ORDER69461-3",
    "psp_ReviewResult" => "A",
    "psp_PosDateTime" => "2019-12-01 12:00:00",
};

my $response = NpsSDK::Nps::notify_fraud_screening_review($params);