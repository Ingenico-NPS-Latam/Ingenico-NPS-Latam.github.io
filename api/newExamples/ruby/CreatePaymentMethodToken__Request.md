require_relative 'lib/nps_sdk'

conf = Nps::Configuration.new
conf.environment =Nps::Environments::STAGING_ENV
conf.key = "_YOUR_SECRET_KEY_"

npssdk = Nps::Sdk.new(conf)

params = {
    'psp_Version' => '2.2',
    'psp_MerchantId' => 'sdk_test',
    'psp_CardInputDetails'  => {
        'Number' => '4507990000000010',
        'ExpirationDate' => '2501',
        'SecurityCode' => '123',
        'HolderName' => 'JOHN DOE'
    },
    'psp_ClientSession' => 'C5jwwbyAYneLbvZe0IYPHTvn7ODMb3vG8ZqCYaYIioUmWUbcgKscGpg8WhXrspRs'
}

begin 
    response = npssdk.create_payment_method_token(params) 
rescue => e 
    puts e.message 
end 
