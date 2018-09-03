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
    "psp_TransactionId" => "65340022",
    "psp_PaymentMethodTag" => "Corporate card",
    "psp_CustomerId" => "bMnVPbNgX55oUz1VLgC41E5iD2rYRo2b",
    "psp_SetAsCustomerDefault" => "1",
    "psp_PosDateTime" => "2008-01-12 13:05:00",
};

my $response = NpsSDK::Nps::create_payment_method_from_payment($params);