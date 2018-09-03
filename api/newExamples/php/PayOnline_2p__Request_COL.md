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
    'psp_MerchTxRef' => 'ORDERX1466Xz-3',
    'psp_MerchOrderId' => 'ORDERX1466Xz',
    'psp_Amount' => '1360000',
    'psp_NumPayments' => '1',
    'psp_Currency' => '170',
    'psp_Country' => 'COL',
    'psp_Product' => '14',
    'psp_CardNumber' => '4005580000050003',
    'psp_CardExpDate' => '1812',
    'psp_PosDateTime' => '2019-12-01 12:00:00',
    'psp_AmountAdditionalDetails' => array(
        'Tip' => '20',
        'Discount' => '1',
        'Taxes' => array(
            array(
                'TypeId' => '100',
                'Amount' => '200000'
            ),
            array(
                'TypeId' => '501',
                'Amount' => '160000',
                'Rate' => '1600',
                'BaseAmount' => '1000000'
            )
        )
    )
);

try{ 
    $response = $sdk->payOnline2p($params); 
}catch(ApiException $e){ 
    echo 'Code to handle error'; 
} 
