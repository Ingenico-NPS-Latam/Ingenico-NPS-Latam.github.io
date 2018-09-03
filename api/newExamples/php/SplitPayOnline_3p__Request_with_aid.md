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
    'psp_MerchOrderId' => 'ORDER66666',
    'psp_ReturnURL' => 'http://localhost/',
    'psp_FrmLanguage' => 'es_AR',
    'psp_Amount' => '15050',
    'psp_Currency' => '032',
    'psp_Country' => 'ARG',
    'psp_Product' => '14',
    'psp_PosDateTime' => '2019-12-01 12:00:00',
    'psp_Transactions' => array(
        array(
            'psp_MerchantId' => 'sdk_test',
            'psp_MerchTxRef' => 'ORDER66666-10',
            'psp_Product' => '14',
            'psp_Amount' => '10000',
            'psp_NumPayments' => '1'
        ),
        array(
            'psp_MerchantId' => 'sdk_test',
            'psp_MerchTxRef' => 'ORDER66666-11',
            'psp_Product' => '14',
            'psp_Amount' => '5050',
            'psp_NumPayments' => '1'
        )
    ),
    'psp_AirlineDetails' => array(
        'PNR' => '154DDD54DWW11',
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
    $response = $sdk->splitPayOnline3p($params); 
}catch(ApiException $e){ 
    echo 'Code to handle error'; 
} 
