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
    'psp_TxSource' => 'WEB',
    'psp_MerchTxRef' => 'ORDERX1466Xz-3',
    'psp_MerchOrderId' => 'ORDERX1466Xz',
    'psp_Amount' => '15050',
    'psp_NumPayments' => '1',
    'psp_Currency' => '032',
    'psp_Country' => 'ARG',
    'psp_Product' => '14',
    'psp_CardNumber' => '4507990000000010',
    'psp_CardExpDate' => '1912',
    'psp_PosDateTime' => '2019-12-01 12:00:00',
    'psp_BillingDetails' => array(
        'Invoice' => '54877555',
        'InvoiceDate' => '2017-10-23',
        'InvoiceAmount' => '15050',
        'InvoiceCurrency' => '032',
        'Person' => array(
            'DateOfBirth' => '1979-01-12',
            'FirstName' => 'John',
            'Gender' => 'M',
            'IDNumber' => '54111111',
            'IDType' => '200',
            'LastName' => 'Doe',
            'MiddleName' => 'Michael',
            'Nationality' => 'ARG',
            'PhoneNumber1' => '+1 011 11111111',
            'PhoneNumber2' => '+1 011 22222222'
            ),
        'Address' => array(
            'AdditionalInfo' => '2 A',
            'City' => 'Miami',
            'Country' => 'USA',
            'HouseNumber' => '1245',
            'StateProvince' => 'Florida',
            'Street' => 'Av. Collins',
            'ZipCode' => '33140'
            )
    ),
    'psp_ShippingDetails' => array(
        'TrackingNumber' => '154DDD54DWW11',
        'Method' => '10',
        'Carrier' => '200',
        'DeliveryDate' => '2014-11-20',
        'FreightAmount' => '15000',
        'GiftMessage' => 'Happy Birthday!',
        'GiftWrapping' => '1',
        'PrimaryRecipient' => array(
            'DateOfBirth' => '1979-01-12',
            'FirstName' => 'John',
            'Gender' => 'M',
            'IDNumber' => '54111111',
            'IDType' => '200',
            'LastName' => 'Doe',
            'MiddleName' => 'Michael',
            'Nationality' => 'ARG',
            'PhoneNumber1' => '+1 011 11111111',
            'PhoneNumber2' => '+1 011 22222222'
            ),
        'SecondaryRecipient' => array(
            'DateOfBirth' => '1979-01-12',
            'FirstName' => 'John',
            'Gender' => 'M',
            'IDNumber' => '54111111',
            'IDType' => '200',
            'LastName' => 'Doe',
            'MiddleName' => 'Michael',
            'Nationality' => 'ARG',
            'PhoneNumber1' => '+1 011 11111111',
            'PhoneNumber2' => '+1 011 22222222'
            ),
        'Address' => array(
            'AdditionalInfo' => '2 A',
            'City' => 'Miami',
            'Country' => 'USA',
            'HouseNumber' => '1245',
            'StateProvince' => 'Florida',
            'Street' => 'Av. Collins',
            'ZipCode' => '33140'
            )
    )
);

try{ 
    $response = $sdk->authorize2p($params) 
}catch(ApiException $e){ 
    echo 'Code to handle error'; 
} 
