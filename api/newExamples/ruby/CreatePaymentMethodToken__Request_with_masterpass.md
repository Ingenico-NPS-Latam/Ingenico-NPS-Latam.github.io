require_relative 'lib/nps_sdk'

conf = Nps::Configuration.new
conf.environment =Nps::Environments::STAGING_ENV
conf.key = "_YOUR_SECRET_KEY_"

npssdk = Nps::Sdk.new(conf)

params = {
    'psp_Version' => '2.2',
    'psp_MerchantId' => 'sdk_test',
    'psp_WalletInputDetails'  => {
        'WalletTypeId' => '2',
        'WalletKey' => 'd084703513e87cd1540a114cd7317e6642eca04e',
        'MerchOrderId' => '1efed583-1824-436a-869f-286ebdb22ae9'
    },
    'psp_ClientSession' => 'C5jwwbyAYneLbvZe0IYPHTvn7ODMb3vG8ZqCYaYIioUmWUbcgKscGpg8WhXrspRs'
}

begin 
    response = npssdk.create_payment_method_token(params) 
rescue => e 
    puts e.message 
end 
