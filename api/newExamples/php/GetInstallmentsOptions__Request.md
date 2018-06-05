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
    'psp_Amount' => '100',
    'psp_Product' => '14',
    'psp_Currency' => '152',
    'psp_Country' => 'CHL',
    'psp_NumPayments' => '1',
    'psp_PaymentMethodToken' => 'KCVMXsbue5fUKOoAxvp1PTJ94gxv2dQM',
    'psp_ClientSession' => 'C5jwwbyAYneLbvZe0IYPHTvn7ODMb3vG8ZqCYaYIioUmWUbcgKscGpg8WhXrspRs',
    'psp_PosDateTime' => '2017-04-04 13:35:20'
);

try{ 
    $response = $sdk->getInstallmentsOptions($params) 
}catch(ApiException $e){ 
    echo 'Code to handle error'; 
} 
