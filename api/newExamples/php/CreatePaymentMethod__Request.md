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
    'psp_PaymentMethod' => array(
        'PaymentMethodToken' => 'HGIYeXKJpQyBvO3pHuZTN9JZiVPnzQaQ',
        'PaymentMethodTag' => 'Corporate card',
        'Person' => array(
            'FirstName' => 'John',
            'LastName' => 'Doe',
            'MiddleName' => 'Michael',
            'PhoneNumber1' => '+1 011 11111111',
            'PhoneNumber2' => '+1 011 22222222',
            'DateOfBirth' => '1979-01-12',
            'Gender' => 'M',
            'Nationality' => 'ARG',
            'IDNumber' => '54111111',
            'IDType' => '200'
            ),
        'Address' => array(
            'Street' => 'Av. Collins',
            'HouseNumber' => '4702',
            'AdditionalInfo' => '2 A',
            'City' => 'Buenos Aires',
            'StateProvince' => 'CABA',
            'Country' => 'ARG',
            'ZipCode' => '1425'
            )
    ),
    'psp_PosDateTime' => '2008-01-12 13:05:00'
);

try{ 
    $response = $sdk->createPaymentMethod($params) 
}catch(ApiException $e){ 
    echo 'Code to handle error'; 
} 
