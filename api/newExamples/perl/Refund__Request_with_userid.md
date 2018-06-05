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
    "psp_MerchTxRef" => "ORDER66666-3",
    "psp_TransactionId_Orig" => "2693348",
    "psp_AmountToRefund" => "15050",
    "psp_UserId" => "john_doe",
    "psp_PosDateTime" => "2019-12-01 12:00:00",
};

my $response = NpsPerlSDK::Nps::refund($params);