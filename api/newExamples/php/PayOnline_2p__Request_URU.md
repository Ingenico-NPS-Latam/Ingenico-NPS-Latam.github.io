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
    'psp_Amount' => '1220000',
    'psp_NumPayments' => '1',
    'psp_Currency' => '858',
    'psp_Country' => 'URY',
    'psp_Product' => '5',
    'psp_CardNumber' => '5453010000083303',
    'psp_CardExpDate' => '1904',
    'psp_PosDateTime' => '2019-12-01 12:00:00',
    'psp_AmountAdditionalDetails' => array(
        'Tip' => '20',
        'Discount' => '1',
        'Taxes' => array(
            array(
                'TypeId' => '601',
                'Amount' => '220000',
                'Rate' => '2200',
                'BaseAmount' => '1000000'
            )
        )
    ),
    'psp_BillingDetails' => array(
        'Invoice' => 'A00024144',
        'InvoiceAmount' => '1600000',
        'InvoiceCurrency' => '858'
    )
);

try{ 
    $response = $sdk->payOnline2p($params); 
}catch(ApiException $e){ 
    echo 'Code to handle error'; 
} 
