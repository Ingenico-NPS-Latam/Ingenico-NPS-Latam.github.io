use NpsSDK\Constants;
use NpsSDK\Configuration;
use NpsSDK\Sdk;
use NpsSDK\ApiException;

Configuration::environment(Constants::STAGING_ENV);
Configuration::secretKey("_YOUR_SECRET_KEY_");
$sdk = new Sdk();

$params = array(
	'psp_Version'=> '2.2',
	'psp_MerchantId'=> 'psp_test',
	'psp_QueryCriteria'=> 'T',
	'psp_QueryCriteriaId'=> '159744',
	'psp_PosDateTime'=> '2019-12-01 12:00:00'
);

try{ 
	$resp = $sdk->queryCardDetails($params) 
}catch(ApiException $e){ 
	echo 'Code to handle error'; 
} 
