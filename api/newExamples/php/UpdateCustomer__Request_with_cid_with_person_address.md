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
    'psp_Person' => array(
        'FirstName' => 'John',
        'LastName' => 'Doe',
        'MiddleName' => 'Michael',
        'PhoneNumber1' => '+1 011 11111111',
        'PhoneNumber2' => '+1 011 22222222',
        'Gender' => 'M',
        'DateOfBirth' => '1979-01-12',
        'Nationality' => 'ARG',
        'IDNumber' => '54111111',
        'IDType' => '200'
    ),
    'psp_Address' => array(
        'Street' => 'Av. Collins',
        'HouseNumber' => '1245',
        'AdditionalInfo' => '2 A',
        'City' => 'Miami',
        'StateProvince' => 'Florida',
        'Country' => 'USA',
        'ZipCode' => '33140'
    ),
    'psp_PaymentMethod' => array(
        'CardInputDetails' => array(
            'Number' => '4507990000000010',
            'ExpirationDate' => '2501',
            'SecurityCode' => '123',
            'HolderName' => 'JOHN DOE'
            ),
        'Person' => array(
            'FirstName' => 'John',
            'LastName' => 'Doe',
            'MiddleName' => 'Michael',
            'PhoneNumber1' => '+1 011 11111111',
            'PhoneNumber2' => '+1 011 22222222',
            'Gender' => 'M',
            'DateOfBirth' => '1979-01-12',
            'Nationality' => 'ARG',
            'IDNumber' => '54111111',
            'IDType' => '200'
            ),
        'Address' => array(
            'Street' => 'Av. Collins',
            'HouseNumber' => '1245',
            'AdditionalInfo' => '2 A',
            'City' => 'Miami',
            'StateProvince' => 'Florida',
            'Country' => 'USA',
            'ZipCode' => '33140'
            )
    ),
    'psp_PosDateTime' => '2008-01-12 13:05:00'
);

try{ 
    $response = $sdk->updateCustomer($params); 
}catch(ApiException $e){ 
    echo 'Code to handle error'; 
} 
