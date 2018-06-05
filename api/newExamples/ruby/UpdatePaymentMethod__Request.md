require_relative 'lib/nps_sdk'

conf = Nps::Configuration.new
conf.environment =Nps::Environments::STAGING_ENV
conf.key = "_YOUR_SECRET_KEY_"

npssdk = Nps::Sdk.new(conf)

params = {
    'psp_Version' => '2.2',
    'psp_MerchantId' => 'sdk_test',
    'psp_PaymentMethodId' => 'Nzmd7DyGytXXC5PtKwnCsXXuQWHJB9EE',
    'psp_PaymentMethodTag' => 'Corporate card',
    'psp_CardInputDetails'  => {
        'ExpirationDate' => '2501'
    },
    'psp_PosDateTime' => '2008-01-12 13:05:00'
}

begin 
    response = npssdk.update_payment_method(params) 
rescue => e 
    puts e.message 
end 
