require_relative 'lib/nps_sdk'

conf = Nps::Configuration.new
conf.environment =Nps::Environments::STAGING_ENV
conf.key = "_YOUR_SECRET_KEY_"

npssdk = Nps::Sdk.new(conf)

params = {
    'psp_Version' => '2.2',
    'psp_MerchantId' => 'sdk_test',
    'psp_TxSource' => 'WEB',
    'psp_MerchTxRef' => 'ORDER69461-3',
    'psp_MerchOrderId' => 'ORDER69461',
    'psp_Amount' => '15050',
    'psp_NumPayments' => '1',
    'psp_Currency' => '032',
    'psp_Country' => 'ARG',
    'psp_Product' => '14',
    'psp_CardNumber' => '4507990000000010',
    'psp_CardExpDate' => '1912',
    'psp_CardSecurityCode' => '325',
    'psp_PosDateTime' => '2019-12-01 12:00:00',
    'psp_3dSecure_XID' => 'MjY0MjAxNjA4MDIyMDUzMzYyNjU=',
    'psp_3dSecure_CAVV' => 'AAABBYZ3N5Qhl3kBU3c3ELGUsMY=',
    'psp_3dSecure_ECI' => '05',
    'psp_3dSecure_Secured' => '1'
}

begin 
    response = npssdk.pay_online_2p(params) 
rescue => e 
    puts e.message 
end 
