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
    'psp_PosDateTime' => '2019-12-01 12:00:00'
);

try{ 
    $response = $sdk->createClientSession($params); 
}catch(ApiException $e){ 
    echo 'Code to handle error'; 
} 
