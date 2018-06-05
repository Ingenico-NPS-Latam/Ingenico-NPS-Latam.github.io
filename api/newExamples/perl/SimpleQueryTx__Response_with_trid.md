use NpsPerlSDK::Nps;
use warnings;
use strict;

my $response = NpsSDK::Nps::simple_query_tx($params);

$response->{psp_ResponseCod};
$response->{psp_ResponseMsg};
$response->{psp_MerchantId};
$response->{psp_QueryCriteria};
$response->{psp_QueryCriteriaId};
$response->{psp_PosDateTime};

my $pspTransaction = $response->{psp_Transaction};
$pspTransaction->{psp_ResponseCod};
$pspTransaction->{psp_ResponseMsg};
$pspTransaction->{psp_ResponseExtended};
$pspTransaction->{psp_TransactionId};
$pspTransaction->{psp_MerchantId};
$pspTransaction->{psp_TxSource};
$pspTransaction->{psp_Operation};
$pspTransaction->{psp_MerchTxRef};
$pspTransaction->{psp_MerchOrderId};
$pspTransaction->{psp_Amount};
$pspTransaction->{psp_NumPayments};
$pspTransaction->{psp_Currency};
$pspTransaction->{psp_Country};
$pspTransaction->{psp_Product};
$pspTransaction->{psp_AuthorizationCode};
$pspTransaction->{psp_BatchNro};
$pspTransaction->{psp_TicketNumber};
$pspTransaction->{psp_CardNumber_FSD};
$pspTransaction->{psp_CardNumber_LFD};
$pspTransaction->{psp_CardMask};
$pspTransaction->{psp_ClExternalMerchant};
$pspTransaction->{psp_ClExternalTerminal};
$pspTransaction->{psp_ClResponseCod};
$pspTransaction->{psp_ClResponseMsg};
$pspTransaction->{psp_PosDateTime};
$pspTransaction->{psp_CreatedAt};

my $pspFraudScreeningResult = $pspTransaction->{psp_FraudScreeningResult};
$pspFraudScreeningResult->{ResultCode};
$pspFraudScreeningResult->{ResultDescription};

my $pspVerificationServicesResult = $pspTransaction->{psp_VerificationServicesResult};
$pspVerificationServicesResult->{ResultCodeCardSecurityCode};
$pspVerificationServicesResult->{ResultCodeBillingAddress};
$pspVerificationServicesResult->{ResultCodeBillingAddressZipCode};
$pspVerificationServicesResult->{ResultCodeBillingPersonIDType};
$pspVerificationServicesResult->{ResultCodeBillingPersonIDNumber};
$pspVerificationServicesResult->{ResultCodeBillingPersonDateOfBirth};
$pspVerificationServicesResult->{ResultCodeBillingPersonName};
$pspVerificationServicesResult->{ResultCodeBillingPersonPhoneNumber1};
$pspVerificationServicesResult->{ResultCodeCustomerEmailAddress};
