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
    "psp_TxSource" => "WEB",
    "psp_MerchOrderId" => "ORDER66666",
    "psp_ReturnURL" => "http://localhost/",
    "psp_FrmLanguage" => "es_AR",
    "psp_Amount" => "15050",
    "psp_Currency" => "032",
    "psp_Country" => "ARG",
    "psp_Product" => "14",
    "psp_PosDateTime" => "2019-12-01 12:00:00",
    "psp_Transactions" => [
        {
            "psp_MerchantId" => "sdk_test",
            "psp_MerchTxRef" => "ORDER66666-3",
            "psp_Product" => "14",
            "psp_Amount" => "10000",
            "psp_NumPayments" => "1",
        },
        {
            "psp_MerchantId" => "sdk_test",
            "psp_MerchTxRef" => "ORDER66666-3",
            "psp_Product" => "14",
            "psp_Amount" => "5050",
            "psp_NumPayments" => "1",
        }
    ],
    "psp_BillingDetails" => {
        "Invoice" => "54877555",
        "InvoiceDate" => "2017-10-23",
        "InvoiceAmount" => "15050",
        "InvoiceCurrency" => "032",
        "Person" => {
            "DateOfBirth" => "1979-01-12",
            "FirstName" => "John",
            "Gender" => "M",
            "IDNumber" => "54111111",
            "IDType" => "200",
            "LastName" => "Doe",
            "MiddleName" => "Michael",
            "Nationality" => "ARG",
            "PhoneNumber1" => "+1 011 11111111",
            "PhoneNumber2" => "+1 011 22222222",
            },
        "Address" => {
            "AdditionalInfo" => "2 A",
            "City" => "Miami",
            "Country" => "USA",
            "HouseNumber" => "1245",
            "StateProvince" => "Florida",
            "Street" => "Av. Collins",
            "ZipCode" => "33140",
            }
    },
    "psp_ShippingDetails" => {
        "TrackingNumber" => "154DDD54DWW11",
        "Method" => "10",
        "Carrier" => "200",
        "DeliveryDate" => "2014-11-20",
        "FreightAmount" => "15000",
        "GiftMessage" => "Happy Birthday!",
        "GiftWrapping" => "1",
        "PrimaryRecipient" => {
            "DateOfBirth" => "1979-01-12",
            "FirstName" => "John",
            "Gender" => "M",
            "IDNumber" => "54111111",
            "IDType" => "200",
            "LastName" => "Doe",
            "MiddleName" => "Michael",
            "Nationality" => "ARG",
            "PhoneNumber1" => "+1 011 11111111",
            "PhoneNumber2" => "+1 011 22222222",
            },
        "SecondaryRecipient" => {
            "DateOfBirth" => "1979-01-12",
            "FirstName" => "John",
            "Gender" => "M",
            "IDNumber" => "54111111",
            "IDType" => "200",
            "LastName" => "Doe",
            "MiddleName" => "Michael",
            "Nationality" => "ARG",
            "PhoneNumber1" => "+1 011 11111111",
            "PhoneNumber2" => "+1 011 22222222",
            },
        "Address" => {
            "AdditionalInfo" => "2 A",
            "City" => "Miami",
            "Country" => "USA",
            "HouseNumber" => "1245",
            "StateProvince" => "Florida",
            "Street" => "Av. Collins",
            "ZipCode" => "33140",
            }
    }
};

my $response = NpsSDK::Nps::split_authorize_3p($params);