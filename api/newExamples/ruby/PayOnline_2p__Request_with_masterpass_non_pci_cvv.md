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
    'psp_Amount' => '15050',
    'psp_NumPayments' => '1',
    'psp_Currency' => '032',
    'psp_Country' => 'ARG',
    'psp_Product' => '5',
    'psp_PosDateTime' => '2019-12-01 12:00:00',
    'psp_CardSecurityCode' => '325',
    'psp_VaultReference'  => {
        'PaymentMethodToken' => 'Nzmd7DyGytXXC5PtKwnCsXXuQWHJB9EE'
    }
}

begin 
    response = npssdk.pay_online_2p(params) 
rescue => e 
    puts e.message 
end 
