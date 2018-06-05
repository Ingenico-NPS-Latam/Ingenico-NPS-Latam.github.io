use NpsSDK\Constants;
use NpsSDK\Configuration;
use NpsSDK\Sdk;
use NpsSDK\ApiException;

Configuration::environment(Constants::STAGING_ENV);
Configuration::secretKey("_YOUR_SECRET_KEY_");
$sdk = new Sdk();

$params = array(
    'psp_Version' => '2.2',
    'psp_MerchantId' => 'sdk_test',
    'psp_TxSource' => 'WEB',
    'psp_MerchTxRef' => 'ORDER69461-3',
    'psp_MerchOrderId' => 'ORDER69461',
    'psp_Amount' => '1200000',
    'psp_NumPayments' => '1',
    'psp_Currency' => '986',
    'psp_Country' => 'BRA',
    'psp_Product' => '14',
    'psp_CardNumber' => '4507990000000010',
    'psp_CardExpDate' => '1912',
    'psp_CardSecurityCode' => '325',
    'psp_PosDateTime' => '2019-12-01 12:00:00',
    'psp_AmountAdditionalDetails' => array(
        'Tip' => '20',
        'Discount' => '1',
        'Taxes' => array(
            array(
                'TypeId' => '100',
                'Amount' => '200000'
            )
        )
    )
);

try{ 
    $response = $sdk->payOnline2p($params) 
}catch(ApiException $e){ 
    echo 'Code to handle error'; 
} 
