use NpsSDK\Constants;
use NpsSDK\Configuration;
use NpsSDK\Sdk;
use NpsSDK\ApiException;

Configuration::environment(Constants::STAGING_ENV);
Configuration::secretKey("_YOUR_SECRET_KEY_");
$sdk = new Sdk();

$params = array(
    'psp_Version' => '2.2',
    'psp_MerchantId' => 'psp_test',
    'psp_TxSource' => 'WEB',
    'psp_MerchTxRef' => 'ORDERX1466Xz-3',
    'psp_MerchOrderId' => 'ORDERX1466Xz',
    'psp_Amount' => '1200000',
    'psp_NumPayments' => '3',
    'psp_CardSecurityCode' => '321',
    'psp_Currency' => '986',
    'psp_Country' => 'BRA',
    'psp_Product' => '5',
    'psp_Plan' => 'CC',
    'psp_CardNumber' => '5453010000083303',
    'psp_CardExpDate' => '1904',
    'psp_PosDateTime' => '2017-03-31 16:14:06',
    'psp_ForceProcessingMethod' => '16',
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
    $response = $sdk->payOnline2p($params); 
}catch(ApiException $e){ 
    echo 'Code to handle error'; 
} 
