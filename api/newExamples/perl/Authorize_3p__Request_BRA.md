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
    "psp_MerchTxRef" => "ORDER76666-3",
    "psp_MerchOrderId" => "ORDER76666",
    "psp_ReturnURL" => "http://localhost/",
    "psp_FrmLanguage" => "es_AR",
    "psp_Amount" => "1200000",
    "psp_NumPayments" => "1",
    "psp_Currency" => "986",
    "psp_Country" => "BRA",
    "psp_Product" => "14",
    "psp_PosDateTime" => "2019-12-01 12:00:00",
    "psp_AmountAdditionalDetails" => {
        "Tip" => "20",
        "Discount" => "1",
        "Taxes" => [
            {
                "TypeId" => "100",
                "Amount" => "200000",
            }
        ]
    }
};

my $response = NpsSDK::Nps::authorize_3p($params);