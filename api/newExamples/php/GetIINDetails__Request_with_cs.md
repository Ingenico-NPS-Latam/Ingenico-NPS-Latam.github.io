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
    'psp_IIN' => '424242',
    'psp_PosDateTime' => '2019-12-01 12:00:00',
    'psp_ClientSession' => 'C5jwwbyAYneLbvZe0IYPHTvn7ODMb3vG8ZqCYaYIioUmWUbcgKscGpg8WhXrspRs'
);

try{ 
    $response = $sdk->getIinDetails($params); 
}catch(ApiException $e){ 
    echo 'Code to handle error'; 
} 
