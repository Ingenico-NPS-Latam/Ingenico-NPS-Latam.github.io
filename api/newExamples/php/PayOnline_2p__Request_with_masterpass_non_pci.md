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
    'psp_Amount' => '15050',
    'psp_NumPayments' => '1',
    'psp_Currency' => '032',
    'psp_Country' => 'ARG',
    'psp_Product' => '5',
    'psp_PosDateTime' => '2019-12-01 12:00:00',
    'psp_VaultReference' => array(
        'PaymentMethodToken' => 'Nzmd7DyGytXXC5PtKwnCsXXuQWHJB9EE'
    )
);

try{ 
    $response = $sdk->payOnline2p($params); 
}catch(ApiException $e){ 
    echo 'Code to handle error'; 
} 
