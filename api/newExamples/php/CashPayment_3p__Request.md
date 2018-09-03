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
    'psp_MerchTxRef' => 'ORDER32145-3',
    'psp_MerchOrderId' => 'ORDER32145',
    'psp_ReturnURL' => 'http://localhost/',
    'psp_FrmLanguage' => 'es_AR',
    'psp_Amount' => '15050',
    'psp_Currency' => '032',
    'psp_Country' => 'ARG',
    'psp_Product' => '301',
    'psp_PosDateTime' => '2019-12-01 12:00:00',
    'psp_FirstExpDate' => '2020-01-01'
);

try{ 
    $response = $sdk->cashPayment3p($params); 
}catch(ApiException $e){ 
    echo 'Code to handle error'; 
} 
