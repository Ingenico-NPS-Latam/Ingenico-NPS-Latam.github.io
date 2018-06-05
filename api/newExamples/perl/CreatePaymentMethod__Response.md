use NpsPerlSDK::Nps;
use warnings;
use strict;

my $response = NpsSDK::Nps::create_payment_method($params);

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
$cardOutputDetails->{HolderName};
$cardOutputDetails->{IIN};
$cardOutputDetails->{Last4};
$cardOutputDetails->{NumberLength};
$cardOutputDetails->{MaskedNumber};
$cardOutputDetails->{MaskedNumberAlternative};
$pspPaymentMethod->{FingerPrint};

my $person = $pspPaymentMethod->{Person};
$person->{FirstName};
$person->{LastName};
$person->{MiddleName};
$person->{PhoneNumber1};
$person->{PhoneNumber2};
$person->{Gender};
$person->{DateOfBirth};
$person->{Nationality};
$person->{IDNumber};
$person->{IDType};

my $address = $pspPaymentMethod->{Address};
$address->{Street};
$address->{HouseNumber};
$address->{AdditionalInfo};
$address->{City};
$address->{StateProvince};
$address->{Country};
$address->{ZipCode};
$pspPaymentMethod->{CreatedAt};
$pspPaymentMethod->{UpdatedAt};
$response->{psp_PosDateTime};
