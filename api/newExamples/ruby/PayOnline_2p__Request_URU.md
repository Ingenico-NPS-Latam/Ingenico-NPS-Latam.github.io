require_relative 'lib/nps_sdk'

conf = Nps::Configuration.new
conf.environment =Nps::Environments::STAGING_ENV
conf.key = "_YOUR_SECRET_KEY_"

npssdk = Nps::Sdk.new(conf)

params = {
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
    'psp_AmountAdditionalDetails'  => {
        'Tip' => '20',
        'Discount' => '1',
        'Taxes'  => [
            {
                'TypeId' => '601',
                'Amount' => '220000',
                'Rate' => '2200',
                'BaseAmount' => '1000000'
            }
        ]
    },
    'psp_BillingDetails'  => {
        'Invoice' => 'A00024144',
        'InvoiceAmount' => '1600000',
        'InvoiceCurrency' => '858'
    }
}

begin 
    response = npssdk.pay_online_2p(params) 
rescue => e 
    puts e.message 
end 
