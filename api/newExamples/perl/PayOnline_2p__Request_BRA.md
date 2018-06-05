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
    "psp_TxSource" => "WEB",
    "psp_MerchTxRef" => "ORDER69461-3",
    "psp_MerchOrderId" => "ORDER69461",
    "psp_Amount" => "1200000",
    "psp_NumPayments" => "1",
    "psp_Currency" => "986",
    "psp_Country" => "BRA",
    "psp_Product" => "14",
    "psp_CardNumber" => "4507990000000010",
    "psp_CardExpDate" => "1912",
    "psp_CardSecurityCode" => "325",
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

my $response = NpsPerlSDK::Nps::pay_online_2p($params);