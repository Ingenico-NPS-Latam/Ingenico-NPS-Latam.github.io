require_relative 'lib/nps_sdk'

conf = Nps::Configuration.new
conf.environment =Nps::Environments::STAGING_ENV
conf.key = "_YOUR_SECRET_KEY_"

npssdk = Nps::Sdk.new(conf)

params = {
    'psp_Version' => '2.2',
    'psp_MerchantId' => 'sdk_test',
    'psp_TransactionId' => '65340022',
    'psp_PaymentMethodTag' => 'Corporate card',
    'psp_CustomerId' => 'bMnVPbNgX55oUz1VLgC41E5iD2rYRo2b',
    'psp_SetAsCustomerDefault' => '1',
    'psp_PosDateTime' => '2008-01-12 13:05:00'
}

begin 
    response = npssdk.create_payment_method_from_payment(params) 
rescue => e 
    puts e.message 
end 
