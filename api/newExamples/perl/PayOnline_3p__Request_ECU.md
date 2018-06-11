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
    "psp_MerchantId" => "psp_test",
    "psp_TxSource" => "WEB",
    "psp_MerchTxRef" => "ORDER76666-3",
    "psp_MerchOrderId" => "ORDER76666",
    "psp_ReturnURL" => "http://localhost/",
    "psp_FrmLanguage" => "es_AR",
    "psp_NumPayments" => "1",
    "psp_Currency" => "840",
    "psp_Country" => "ECU",
    "psp_Product" => "14",
    "psp_PosDateTime" => "2019-12-01 12:00:00",
    "psp_Amount" => "31200",
    "psp_AmountAdditionalDetails" => {
        "Taxes" => [
            {
                "TypeId" => "700",
                "Amount" => "1200",
                "Rate" => "1200",
                "BaseAmount" => "100000",
            },
            {
                "TypeId" => "701",
                "BaseAmount" => "20000",
            }
        ]
    }
};

my $response = NpsPerlSDK::Nps::pay_online_3p($params);