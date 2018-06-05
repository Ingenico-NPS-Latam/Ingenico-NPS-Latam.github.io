require_relative 'lib/nps_sdk'

conf = Nps::Configuration.new
conf.environment =Nps::Environments::STAGING_ENV
conf.key = "_YOUR_SECRET_KEY_"

npssdk = Nps::Sdk.new(conf)

params = {
    'psp_Version' => '2.2',
    'psp_MerchantId' => 'sdk_test',
    'psp_TxSource' => 'WEB',
    'psp_MerchTxRef' => 'ORDER66666-3',
    'psp_TransactionId_Orig' => '2693348',
    'psp_AmountToCapture' => '15050',
    'psp_UserId' => 'john_doe',
    'psp_PosDateTime' => '2019-12-01 12:00:00'
}

begin 
    response = npssdk.capture(params) 
rescue => e 
    puts e.message 
end 
