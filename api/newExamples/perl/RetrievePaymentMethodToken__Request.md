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
    "psp_PaymentMethodToken" => "KCVMXsbue5fUKOoAxvp1PTJ94gxv2dQM",
    "psp_ClientSession" => "C5jwwbyAYneLbvZe0IYPHTvn7ODMb3vG8ZqCYaYIioUmWUbcgKscGpg8WhXrspRs",
};

my $response = NpsPerlSDK::Nps::retrieve_payment_method_token($params);