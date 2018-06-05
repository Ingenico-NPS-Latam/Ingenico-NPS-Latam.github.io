require_relative 'lib/nps_sdk'

conf = Nps::Configuration.new
conf.environment =Nps::Environments::STAGING_ENV
conf.key = "_YOUR_SECRET_KEY_"

npssdk = Nps::Sdk.new(conf)

params = {
	'psp_Version'=> '2.2',
	'psp_MerchantId'=> 'psp_test',
	'psp_QueryCriteria'=> 'T',
	'psp_QueryCriteriaId'=> '159744',
	'psp_PosDateTime'=> '2019-12-01 12:00:00'
}

begin 
	resp = npssdk.query_card_details(params) 
rescue => e 
	puts e.message 
end 
