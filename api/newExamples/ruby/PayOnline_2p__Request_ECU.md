require_relative 'lib/nps_sdk'

conf = Nps::Configuration.new
conf.environment =Nps::Environments::STAGING_ENV
conf.key = "_YOUR_SECRET_KEY_"

npssdk = Nps::Sdk.new(conf)

params = {
    'psp_Version' => '2.2',
    'psp_MerchantId' => 'psp_test',
    'psp_TxSource' => 'WEB',
    'psp_MerchTxRef' => 'ORDERX1466Xz-3',
    'psp_MerchOrderId' => 'ORDERX1466Xz',
    'psp_NumPayments' => '1',
    'psp_Currency' => '840',
    'psp_Country' => 'ECU',
    'psp_Product' => '5',
    'psp_CardNumber' => '5189680000495961',
    'psp_CardExpDate' => '3311',
    'psp_PosDateTime' => '2019-12-01 12:00:00',
    'psp_Amount' => '31200',
    'psp_AmountAdditionalDetails'  => {
        'Taxes'  => [
            {
                'TypeId' => '700',
                'Amount' => '1200',
                'Rate' => '1200',
                'BaseAmount' => '100000'
            },
            {
                'TypeId' => '701',
                'BaseAmount' => '20000'
            }
        ]
    }
}

begin 
    response = npssdk.pay_online_2p(params) 
rescue => e 
    puts e.message 
end 
