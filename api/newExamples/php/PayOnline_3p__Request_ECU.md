use NpsSDK\Constants;
use NpsSDK\Configuration;
use NpsSDK\Sdk;
use NpsSDK\ApiException;

Configuration::environment(Constants::STAGING_ENV);
Configuration::secretKey("_YOUR_SECRET_KEY_");
$sdk = new Sdk();

$params = array(
    'psp_Version' => '2.2',
    'psp_MerchantId' => 'psp_test',
    'psp_TxSource' => 'WEB',
    'psp_MerchTxRef' => 'ORDER76666-3',
    'psp_MerchOrderId' => 'ORDER76666',
    'psp_ReturnURL' => 'http://localhost/',
    'psp_FrmLanguage' => 'es_AR',
    'psp_NumPayments' => '1',
    'psp_Currency' => '840',
    'psp_Country' => 'ECU',
    'psp_Product' => '14',
    'psp_PosDateTime' => '2019-12-01 12:00:00',
    'psp_Amount' => '31200',
    'psp_AmountAdditionalDetails' => array(
        'Taxes' => array(
            array(
                'TypeId' => '700',
                'Amount' => '1200',
                'Rate' => '1200',
                'BaseAmount' => '10000'
            ),
            array(
                'TypeId' => '701',
                'BaseAmount' => '20000'
            )
        )
    )
);

try{ 
    $response = $sdk->payOnline3p($params); 
}catch(ApiException $e){ 
    echo 'Code to handle error'; 
} 
