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
    'psp_Person' => array(
        'FirstName' => 'John',
        'LastName' => 'Doe',
        'MiddleName' => 'Michael',
        'DateOfBirth' => '1979-01-12',
        'PhoneNumber1' => '+1 011 11111111',
        'PhoneNumber2' => '+1 011 22222222',
        'Gender' => 'M',
        'Nationality' => 'ARG',
        'IDNumber' => '54111111',
        'IDType' => '200'
    ),
    'psp_Address' => array(
        'Street' => 'Av. Collins',
        'HouseNumber' => '4702',
        'AdditionalInfo' => '2 A',
        'City' => 'Buenos Aires',
        'StateProvince' => 'CABA',
        'Country' => 'ARG',
        'ZipCode' => '1425'
    ),
    'psp_ClientSession' => 'C5jwwbyAYneLbvZe0IYPHTvn7ODMb3vG8ZqCYaYIioUmWUbcgKscGpg8WhXrspRs'
);

try{ 
    $response = $sdk->createPaymentMethodToken($params) 
}catch(ApiException $e){ 
    echo 'Code to handle error'; 
} 
