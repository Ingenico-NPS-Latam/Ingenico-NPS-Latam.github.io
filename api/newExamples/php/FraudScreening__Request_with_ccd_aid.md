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
    'psp_MerchTxRef' => 'ORDER66666-3',
    'psp_MerchOrderId' => 'ORDER66666',
    'psp_Amount' => '15050',
    'psp_NumPayments' => '1',
    'psp_Currency' => '032',
    'psp_Country' => 'ARG',
    'psp_Product' => '14',
    'psp_CardNumber' => '4507990000000010',
    'psp_CardExpDate' => '1912',
    'psp_PosDateTime' => '2916-12-01 12:00:00',
    'psp_CustomerAdditionalDetails' => array(
        'EmailAddress' => 'jdoe@email.com',
        'AlternativeEmailAddress' => 'Jdoe79@email.com',
        'IPAddress' => '192.168.158.190',
        'AccountID' => 'Jdoe78',
        'AccountCreatedAt' => '2010-10-23',
        'AccountPreviousActivity' => '1',
        'AccountHasCredentials' => '1',
        'DeviceType' => '1',
        'DeviceFingerPrint' => 'KJhKHKJgh7777kgh...',
        'BrowserLanguage' => 'ES',
        'HttpUserAgent' => 'Mozilla/5.0 (X11; Ubuntu; Linux x86_64; rv:21.0) Gecko/20100101 Firefox/21.0'
    ),
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
    'psp_AirlineDetails' => array(
        'PNR' => '154DDD54DWW11',
        'Legs' => array(
            array(
                'DepartureAirport' => 'EZE',
                'DepartureDatetime' => '2014-05-12 13:05:00',
                'DepartureAirportTimezone' => '-03:00',
                'ArrivalAirport' => 'AMS',
                'CarrierCode' => 'KL',
                'FlightNumber' => '842',
                'FareBasisCode' => 'HL7LNR',
                'FareClassCode' => 'FR',
                'BaseFare' => '30000',
                'BaseFareCurrency' => '032'
            )
        ),
        'Passengers' => array(
            array(
                'FirstName' => 'John',
                'LastName' => 'Doe',
                'MiddleName' => 'Michael',
                'Type' => 'A',
                'DateOfBirth' => '1979-01-12',
                'Nationality' => 'ARG',
                'IDNumber' => '54111111',
                'IDType' => '100',
                'IDCountry' => 'ARG',
                'LoyaltyNumber' => '254587547',
                'LoyaltyTier' => '1'
            )
        ),
        'Ticket' => array(
            'TicketNumber' => '07411865255578',
            'Eticket' => '1',
            'Restricted' => '1',
            'Issue' => array(
                'TravelAgentCode' => '32165464',
                'TravelAgentName' => 'Washington Hilton',
                'Date' => '2017-01-10',
                'Country' => 'ARG',
                'City' => 'Buenos Aires',
                'Address' => 'Av. Rivadavia 1111'
                    ),
            'TotalFareAmount' => '80000',
            'TotalTaxAmount' => '25200',
            'TotalFeeAmount' => '14800'
            )
    )
);

try{ 
    $response = $sdk->fraudScreening($params) 
}catch(ApiException $e){ 
    echo 'Code to handle error'; 
} 
