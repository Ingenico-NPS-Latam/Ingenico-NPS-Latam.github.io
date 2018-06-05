require_relative 'lib/nps_sdk'

conf = Nps::Configuration.new
conf.environment =Nps::Environments::STAGING_ENV
conf.key = "_YOUR_SECRET_KEY_"

npssdk = Nps::Sdk.new(conf)

params = {
    'psp_Version' => '2.2',
    'psp_MerchantId' => 'sdk_test',
    'psp_Amount' => '100',
    'psp_Product' => '14',
    'psp_Currency' => '152',
    'psp_Country' => 'CHL',
    'psp_NumPayments' => '12',
    'psp_PaymentMethodToken' => 'KCVMXsbue5fUKOoAxvp1PTJ94gxv2dQM',
    'psp_ClientSession' => 'C5jwwbyAYneLbvZe0IYPHTvn7ODMb3vG8ZqCYaYIioUmWUbcgKscGpg8WhXrspRs',
    'psp_PosDateTime' => '2017-04-04 13:35:20'
}

begin 
    response = npssdk.get_installments_options(params) 
rescue => e 
    puts e.message 
end 
