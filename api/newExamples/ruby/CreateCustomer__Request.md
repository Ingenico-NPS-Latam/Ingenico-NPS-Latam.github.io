require_relative 'lib/nps_sdk'

conf = Nps::Configuration.new
conf.environment =Nps::Environments::STAGING_ENV
conf.key = "_YOUR_SECRET_KEY_"

npssdk = Nps::Sdk.new(conf)

params = {
    'psp_Version' => '2.2',
    'psp_MerchantId' => 'sdk_test',
    'psp_EmailAddress' => 'jhon.doe@example.com',
    'psp_AlternativeEmailAddress' => 'jdoe@example.com',
    'psp_AccountID' => 'jdoe78',
    'psp_AccountCreatedAt' => '2010-10-23',
    'psp_PaymentMethod'  => {
        'PaymentMethodToken' => 'KCVMXsbue5fUKOoAxvp1PTJ94gxv2dQM'
    },
    'psp_PosDateTime' => '2008-01-12 13:05:00'
}

begin 
    response = npssdk.create_customer(params) 
rescue => e 
    puts e.message 
end 
