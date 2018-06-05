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
    'psp_CardInputDetails' => array(
        'Number' => '4507990000000010',
        'ExpirationDate' => '2501',
        'SecurityCode' => '123',
        'HolderName' => 'JOHN DOE'
    ),
    'psp_ClientSession' => 'C5jwwbyAYneLbvZe0IYPHTvn7ODMb3vG8ZqCYaYIioUmWUbcgKscGpg8WhXrspRs'
);

try{ 
    $response = $sdk->createPaymentMethodToken($params) 
}catch(ApiException $e){ 
    echo 'Code to handle error'; 
} 
