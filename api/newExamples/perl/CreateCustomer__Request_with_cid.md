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
    "psp_EmailAddress" => "jhon.doe@example.com",
    "psp_AlternativeEmailAddress" => "jdoe@example.com",
    "psp_AccountID" => "jdoe78",
    "psp_AccountCreatedAt" => "2010-10-23",
    "psp_PaymentMethod" => {
        "CardInputDetails" => {
            "Number" => "4507990000000010",
            "ExpirationDate" => "2501",
            "SecurityCode" => "123",
            "HolderName" => "JOHN DOE",
            }
    },
    "psp_PosDateTime" => "2008-01-12 13:05:00",
};

my $response = NpsPerlSDK::Nps::create_customer($params);