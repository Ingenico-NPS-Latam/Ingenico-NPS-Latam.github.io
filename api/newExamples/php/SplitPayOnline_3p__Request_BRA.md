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
    'psp_Amount' => '2400000',
    'psp_Currency' => '986',
    'psp_Country' => 'BRA',
    'psp_Product' => '14',
    'psp_PosDateTime' => '2019-12-01 12:00:00',
    'psp_Transactions' => array(
        array(
            'psp_MerchantId' => 'sdk_test',
            'psp_MerchTxRef' => 'ORDER66666-3',
            'psp_Product' => '14',
            'psp_Amount' => '1200000',
            'psp_NumPayments' => '1',
            'psp_AmountAdditionalDetails' => array(
                'Tip' => '20',
                'Discount' => '1',
                'Taxes' => array(
                    array(
                        'TypeId' => '100',
                        'Amount' => '200000'
                    )
                )
                    )
        ),
        array(
            'psp_MerchantId' => 'sdk_test',
            'psp_MerchTxRef' => 'ORDER66666-3',
            'psp_Product' => '14',
            'psp_Amount' => '1200000',
            'psp_NumPayments' => '1',
            'psp_AmountAdditionalDetails' => array(
                'Tip' => '20',
                'Discount' => '1',
                'Taxes' => array(
                    array(
                        'TypeId' => '100',
                        'Amount' => '200000'
                    )
                )
                    )
        ),
    )
);

try{ 
    $response = $sdk->splitPayOnline3p($params); 
}catch(ApiException $e){ 
    echo 'Code to handle error'; 
} 
