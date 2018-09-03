use NpsSDK::Nps;
use warnings;
use strict;

my $response = NpsSDK::Nps::split_pay_online_3p($params);

$response->{psp_ResponseCod};
$response->{psp_ResponseMsg};
$response->{psp_TransactionId};
$response->{psp_Session3p};
$response->{psp_FrontPSP_URL};
$response->{psp_MerchantId};
$response->{psp_MerchTxRef};
$response->{psp_MerchOrderId};
$response->{psp_Amount};
$response->{psp_Currency};
$response->{psp_Country};
$response->{psp_Product};
$response->{psp_CustomerMail};
$response->{psp_PosDateTime};

my $pspTransactions0 = $response->{psp_Transactions}[0];

$pspTransactions0->{psp_MerchantId};
$pspTransactions0->{psp_TransactionId};
$pspTransactions0->{psp_MerchTxRef};
$pspTransactions0->{psp_Product};
$pspTransactions0->{psp_Amount};
$pspTransactions0->{psp_NumPayments};
$pspTransactions0->{psp_CreatedAt};
my $pspTransactions1 = $response->{psp_Transactions}[1];

$pspTransactions1->{psp_MerchantId};
$pspTransactions1->{psp_TransactionId};
$pspTransactions1->{psp_MerchTxRef};
$pspTransactions1->{psp_Product};
$pspTransactions1->{psp_Amount};
$pspTransactions1->{psp_NumPayments};
$pspTransactions1->{psp_CreatedAt};

