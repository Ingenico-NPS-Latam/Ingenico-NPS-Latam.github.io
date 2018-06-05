require_relative 'lib/nps_sdk'

conf = Nps::Configuration.new
conf.environment =Nps::Environments::STAGING_ENV
conf.key = "_YOUR_SECRET_KEY_"

npssdk = Nps::Sdk.new(conf)

params = {
    'psp_Version' => '2.2',
    'psp_MerchantId' => 'sdk_test',
    'psp_Criteria' => 'T',
    'psp_CriteriaId' => 'ORDER69461-3',
    'psp_ReviewResult' => 'A',
    'psp_PosDateTime' => '2019-12-01 12:00:00'
}

begin 
    resp = npssdk.notify_fraud_screening_review(params) 
rescue => e 
    puts e.message 
end 
