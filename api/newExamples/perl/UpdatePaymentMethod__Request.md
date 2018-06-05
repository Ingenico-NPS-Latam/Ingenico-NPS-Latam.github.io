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
    "psp_PaymentMethodId" => "Nzmd7DyGytXXC5PtKwnCsXXuQWHJB9EE",
    "psp_PaymentMethodTag" => "Corporate card",
    "psp_CardInputDetails" => {
        "ExpirationDate" => "2501",
    },
    "psp_PosDateTime" => "2008-01-12 13:05:00",
};

my $response = NpsPerlSDK::Nps::update_payment_method($params);