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
    "psp_CardInputDetails" => {
        "Number" => "4507990000000010",
        "ExpirationDate" => "2501",
        "SecurityCode" => "123",
        "HolderName" => "JOHN DOE",
    },
    "psp_ClientSession" => "C5jwwbyAYneLbvZe0IYPHTvn7ODMb3vG8ZqCYaYIioUmWUbcgKscGpg8WhXrspRs",
};

my $response = NpsPerlSDK::Nps::create_payment_method_token($params);