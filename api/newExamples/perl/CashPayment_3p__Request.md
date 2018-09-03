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
    "psp_MerchTxRef" => "ORDER32145-3",
    "psp_MerchOrderId" => "ORDER32145",
    "psp_ReturnURL" => "http://localhost/",
    "psp_FrmLanguage" => "es_AR",
    "psp_Amount" => "15050",
    "psp_Currency" => "032",
    "psp_Country" => "ARG",
    "psp_Product" => "301",
    "psp_PosDateTime" => "2019-12-01 12:00:00",
    "psp_FirstExpDate" => "2020-01-01",
};

my $response = NpsSDK::Nps::cash_payment_3p($params);