require_relative 'lib/nps_sdk'

conf = Nps::Configuration.new
conf.environment =Nps::Environments::STAGING_ENV
conf.key = "_YOUR_SECRET_KEY_"

npssdk = Nps::Sdk.new(conf)

params = {
    'psp_Version' => '2.2',
    'psp_MerchantId' => 'sdk_test',
    'psp_CustomerId' => 'bMnVPbNgX55oUz1VLgC41E5iD2rYRo2b',
    'psp_EmailAddress' => 'jhon.doe@example.com',
    'psp_AlternativeEmailAddress' => 'jdoe@example.com',
    'psp_AccountCreatedAt' => '2010-10-23',
    'psp_AccountID' => 'jdoe78',
    'psp_PaymentMethod'  => {
        'PaymentMethodToken' => 'vp1PTJuKCVMXsbeOoAx94gxv2dQM5fUK'
    },
    'psp_PosDateTime' => '2008-01-12 13:05:00'
}

begin 
    response = npssdk.update_customer(params) 
rescue => e 
    puts e.message 
end 
