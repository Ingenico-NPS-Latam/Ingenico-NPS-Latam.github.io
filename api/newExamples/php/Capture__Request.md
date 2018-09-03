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
    'psp_MerchTxRef' => 'ORDER66666-3',
    'psp_TransactionId_Orig' => '2693348',
    'psp_AmountToCapture' => '15050',
    'psp_PosDateTime' => '2019-12-01 12:00:00'
);

try{ 
    $response = $sdk->capture($params); 
}catch(ApiException $e){ 
    echo 'Code to handle error'; 
} 
