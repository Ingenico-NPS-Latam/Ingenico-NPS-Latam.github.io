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
    'psp_TransactionId' => '65340022',
    'psp_PaymentMethodTag' => 'Corporate card',
    'psp_CustomerId' => 'bMnVPbNgX55oUz1VLgC41E5iD2rYRo2b',
    'psp_SetAsCustomerDefault' => '1',
    'psp_PosDateTime' => '2008-01-12 13:05:00'
);

try{ 
    $response = $sdk->createPaymentMethodFromPayment($params) 
}catch(ApiException $e){ 
    echo 'Code to handle error'; 
} 
