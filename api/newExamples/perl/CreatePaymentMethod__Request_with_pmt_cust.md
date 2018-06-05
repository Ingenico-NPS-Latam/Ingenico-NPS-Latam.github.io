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
    "psp_PaymentMethod" => {
        "PaymentMethodToken" => "HGIYeXKJpQyBvO3pHuZTN9JZiVPnzQaQ",
        "PaymentMethodTag" => "Corporate card",
        "Person" => {
            "FirstName" => "John",
            "LastName" => "Doe",
            "MiddleName" => "Michael",
            "PhoneNumber1" => "+1 011 11111111",
            "PhoneNumber2" => "+1 011 22222222",
            "DateOfBirth" => "1979-01-12",
            "Gender" => "M",
            "Nationality" => "ARG",
            "IDNumber" => "54111111",
            "IDType" => "200",
            },
        "Address" => {
            "Street" => "Av. Collins",
            "HouseNumber" => "4702",
            "AdditionalInfo" => "2 A",
            "City" => "Buenos Aires",
            "StateProvince" => "CABA",
            "Country" => "ARG",
            "ZipCode" => "1425",
            }
    },
    "psp_SetAsCustomerDefault" => "1",
    "psp_PosDateTime" => "2008-01-12 13:05:00",
};

my $response = NpsPerlSDK::Nps::create_payment_method($params);