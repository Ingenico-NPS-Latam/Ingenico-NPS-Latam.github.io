use NpsPerlSDK::Nps;
use warnings;
use strict;

NpsPerlSDK::Configuration::configure(environment => $constants::SANDBOX_ENV,
									 secret_key => "_YOUR_SECRET_KEY_",
									 sanitize => 1 
									 );

my $params = {
	"psp_Version" => "2.2",
	"psp_MerchantId" => "psp_test",
	"psp_QueryCriteria" => "T",
	"psp_QueryCriteriaId" => "159744",
	"psp_PosDateTime" => "2019-12-01 12:00:00",
};

my $response = NpsPerlSDK::Nps::query_card_details($params);
