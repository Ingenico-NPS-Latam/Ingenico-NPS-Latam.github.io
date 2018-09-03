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
    'psp_CustomerId' => 'bMnVPbNgX55oUz1VLgC41E5iD2rYRo2b',
    'psp_EmailAddress' => 'jhon.doe@example.com',
    'psp_AlternativeEmailAddress' => 'jdoe@example.com',
    'psp_AccountCreatedAt' => '2010-10-23',
    'psp_AccountID' => 'jdoe78',
    'psp_PaymentMethod' => array(
        'CardInputDetails' => array(
            'Number' => '4507990000000010',
            'ExpirationDate' => '2501',
            'SecurityCode' => '123',
            'HolderName' => 'JOHN DOE'
            )
    ),
    'psp_PosDateTime' => '2008-01-12 13:05:00'
);

try{ 
    $response = $sdk->updateCustomer($params); 
}catch(ApiException $e){ 
    echo 'Code to handle error'; 
} 
