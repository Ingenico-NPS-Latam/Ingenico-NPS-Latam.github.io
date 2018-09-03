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
    "psp_NewSecretKey" => "YOUR_NEW_SECRET_KEY",
    "psp_PosDateTime" => "2019-12-01 12:00:00",
};

my $response = NpsSDK::Nps::change_secret_key($params);