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
    "psp_CustomerId" => "bMnVPbNgX55oUz1VLgC41E5iD2rYRo2b",
    "psp_PosDateTime" => "2008-01-12 13:05:00",
};

my $response = NpsPerlSDK::Nps::delete_customer($params);