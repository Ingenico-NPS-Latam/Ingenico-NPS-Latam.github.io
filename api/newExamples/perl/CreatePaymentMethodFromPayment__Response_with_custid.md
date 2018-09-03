use NpsSDK::Nps;
use warnings;
use strict;

my $response = NpsSDK::Nps::create_payment_method_from_payment($params);

$response->{psp_ResponseCod};
$response->{psp_ResponseMsg};
$response->{psp_MerchantId};

my $pspPaymentMethod = $response->{psp_PaymentMethod};
$pspPaymentMethod->{PaymentMethodId};
$pspPaymentMethod->{PaymentMethodTag};
$pspPaymentMethod->{Product};

my $cardOutputDetails = $pspPaymentMethod->{CardOutputDetails};
$cardOutputDetails->{ExpirationDate};
$cardOutputDetails->{ExpirationYear};
$cardOutputDetails->{ExpirationMonth};
$cardOutputDetails->{IIN};
$cardOutputDetails->{Last4};
$cardOutputDetails->{NumberLength};
$cardOutputDetails->{MaskedNumber};
$cardOutputDetails->{MaskedNumberAlternative};
$pspPaymentMethod->{FingerPrint};
$pspPaymentMethod->{CreatedAt};
$pspPaymentMethod->{UpdatedAt};
$response->{psp_CustomerId};
$response->{psp_PosDateTime};
