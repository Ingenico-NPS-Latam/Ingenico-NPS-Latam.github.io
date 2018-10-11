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
    "psp_WalletInputDetails" => {
        "WalletTypeId" => "2",
        "WalletKey" => "d084703513e87cd1540a114cd7317e6642eca04e",
        "MerchOrderId" => "1efed583-1824-436a-869f-286ebdb22ae9",
    },
    "psp_ClientSession" => "C5jwwbyAYneLbvZe0IYPHTvn7ODMb3vG8ZqCYaYIioUmWUbcgKscGpg8WhXrspRs",
};

my $response = NpsSDK::Nps::create_payment_method_token($params);