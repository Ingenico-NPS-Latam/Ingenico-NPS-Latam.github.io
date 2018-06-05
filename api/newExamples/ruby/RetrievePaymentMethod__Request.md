require_relative 'lib/nps_sdk'

conf = Nps::Configuration.new
conf.environment =Nps::Environments::STAGING_ENV
conf.key = "_YOUR_SECRET_KEY_"

npssdk = Nps::Sdk.new(conf)

params = {
    'psp_Version' => '2.2',
    'psp_MerchantId' => 'sdk_test',
    'psp_PaymentMethodId' => 'jGW24iDaoMBzfKHViL18TmHo9sHBgW4J',
    'psp_PosDateTime' => '2008-01-12 13:05:00'
}

begin 
    response = npssdk.retrieve_payment_method(params) 
rescue => e 
    puts e.message 
end 
