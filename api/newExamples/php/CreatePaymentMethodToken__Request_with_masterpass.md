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
    'psp_WalletInputDetails' => array(
        'WalletTypeId' => '2',
        'WalletKey' => 'd084703513e87cd1540a114cd7317e6642eca04e',
        'MerchOrderId' => '1efed583-1824-436a-869f-286ebdb22ae9'
    ),
    'psp_ClientSession' => 'C5jwwbyAYneLbvZe0IYPHTvn7ODMb3vG8ZqCYaYIioUmWUbcgKscGpg8WhXrspRs'
);

try{ 
    $response = $sdk->createPaymentMethodToken($params); 
}catch(ApiException $e){ 
    echo 'Code to handle error'; 
} 
