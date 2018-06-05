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
    "psp_PosDateTime" => "2019-12-01 12:00:00",
    "psp_CustomerId" => "K8sj5rBrGqPBczTR4LtuKE6g4iZMmY9f",
};

my $response = NpsPerlSDK::Nps::create_client_session($params);