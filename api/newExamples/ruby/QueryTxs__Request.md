require_relative 'lib/nps_sdk'

conf = Nps::Configuration.new
conf.environment =Nps::Environments::STAGING_ENV
conf.key = "_YOUR_SECRET_KEY_"

npssdk = Nps::Sdk.new(conf)

params = {
    'psp_Version' => '2.2',
    'psp_MerchantId' => 'sdk_test',
    'psp_QueryCriteria' => 'O',
    'psp_QueryCriteriaId' => 'ORDER69461-3',
    'psp_PosDateTime' => '2019-12-01 12:00:00'
}

begin 
    response = npssdk.query_txs(params) 
rescue => e 
    puts e.message 
end 
