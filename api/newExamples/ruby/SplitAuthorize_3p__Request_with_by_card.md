require_relative 'lib/nps_sdk'

conf = Nps::Configuration.new
conf.environment =Nps::Environments::STAGING_ENV
conf.key = "_YOUR_SECRET_KEY_"

npssdk = Nps::Sdk.new(conf)

params = {
    'psp_Version' => '2.2',
    'psp_MerchantId' => 'sdk_test',
    'psp_TxSource' => 'WEB',
    'psp_MerchOrderId' => 'ORDER66666',
    'psp_ReturnURL' => 'http://localhost/',
    'psp_FrmLanguage' => 'es_AR',
    'psp_Amount' => '15050',
    'psp_Currency' => '032',
    'psp_Country' => 'ARG',
    'psp_UseMultipleProducts' => '1',
    'psp_Product' => '14',
    'psp_PosDateTime' => '2019-12-01 12:00:00',
    'psp_Transactions'  => [
        {
            'psp_MerchTxRef' => 'ORDER66666-3',
            'psp_Product' => '14',
            'psp_Amount' => '10000',
            'psp_NumPayments' => '1'
        },
        {
            'psp_MerchTxRef' => 'ORDER66666-4',
            'psp_Product' => '14',
            'psp_Amount' => '5050',
            'psp_NumPayments' => '12'
        }
    ]
}

begin 
    response = npssdk.split_authorize_3p(params) 
rescue => e 
    puts e.message 
end 
