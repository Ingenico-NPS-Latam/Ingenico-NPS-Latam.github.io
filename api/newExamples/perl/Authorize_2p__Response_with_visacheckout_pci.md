use NpsSDK::Nps;
use warnings;
use strict;

my $response = NpsSDK::Nps::authorize_2p($params);

$response->{psp_ResponseCod};
$response->{psp_ResponseMsg};
$response->{psp_ResponseExtended};
$response->{psp_TransactionId};
$response->{psp_MerchantId};
$response->{psp_MerchTxRef};
$response->{psp_MerchOrderId};
$response->{psp_Amount};
$response->{psp_NumPayments};
$response->{psp_Currency};
$response->{psp_Country};
$response->{psp_Product};
$response->{psp_CardNumber};
$response->{psp_CardExpDate};
$response->{psp_AuthorizationCode};
$response->{psp_BatchNro};
$response->{psp_TicketNumber};
$response->{psp_ClExternalMerchant};
$response->{psp_ClExternalTerminal};
$response->{psp_ClResponseCod};
$response->{psp_ClResponseMsg};
$response->{psp_PosDateTime};
$response->{psp_CreatedAt};

my $pspFraudScreeningResult = $response->{psp_FraudScreeningResult};
$pspFraudScreeningResult->{ResultCode};
$pspFraudScreeningResult->{ResultDescription};

my $pspVerificationServicesResult = $response->{psp_VerificationServicesResult};
$pspVerificationServicesResult->{ResultCodeCardSecurityCode};
$pspVerificationServicesResult->{ResultCodeBillingAddress};
$pspVerificationServicesResult->{ResultCodeBillingAddressZipCode};
$pspVerificationServicesResult->{ResultCodeBillingPersonIDType};
$pspVerificationServicesResult->{ResultCodeBillingPersonIDNumber};
$pspVerificationServicesResult->{ResultCodeBillingPersonDateOfBirth};
$pspVerificationServicesResult->{ResultCodeBillingPersonName};
$pspVerificationServicesResult->{ResultCodeBillingPersonPhoneNumber1};
$pspVerificationServicesResult->{ResultCodeCustomerEmailAddress};
