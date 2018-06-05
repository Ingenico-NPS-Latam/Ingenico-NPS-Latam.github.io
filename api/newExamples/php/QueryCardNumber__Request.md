use NpsSDK\Constants;
use NpsSDK\Configuration;
use NpsSDK\Sdk;
use NpsSDK\ApiException;

Configuration::environment(Constants::STAGING_ENV);
Configuration::secretKey("_YOUR_SECRET_KEY_");
$sdk = new Sdk();

$params = array(
    'psp_Version' => '1',
    'psp_MerchantId' => 'sdk_test',
    'psp_QueryCriteria' => 'T',
    'psp_QueryCriteriaId' => '76577',
    'psp_PosDateTime' => '2019-12-01 12:00:00'
);

try{ 
    $response = $sdk->queryCardNumber($params) 
}catch(ApiException $e){ 
    echo 'Code to handle error'; 
} 
