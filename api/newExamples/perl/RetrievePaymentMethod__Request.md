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
    "psp_PaymentMethodId" => "jGW24iDaoMBzfKHViL18TmHo9sHBgW4J",
    "psp_PosDateTime" => "2008-01-12 13:05:00",
};

my $response = NpsSDK::Nps::retrieve_payment_method($params);