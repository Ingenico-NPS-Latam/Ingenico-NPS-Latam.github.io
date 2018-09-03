use NpsSDK::Nps;
use warnings;
use strict;

my $response = NpsSDK::Nps::update_customer($params);

$response->{psp_ResponseCod};
$response->{psp_ResponseMsg};
$response->{psp_MerchantId};
$response->{psp_CustomerId};
$response->{psp_EmailAddress};
$response->{psp_AlternativeEmailAddress};
$response->{psp_AccountID};
$response->{psp_AccountCreatedAt};
$response->{psp_DefaultPaymentMethodId};

my $pspPaymentMethods0 = $response->{psp_PaymentMethods}[0];

$pspPaymentMethods0->{PaymentMethodId};
$pspPaymentMethods0->{Product};

my $cardOutputDetails = $pspPaymentMethods0->{CardOutputDetails};
$cardOutputDetails->{ExpirationDate};
$cardOutputDetails->{ExpirationYear};
$cardOutputDetails->{ExpirationMonth};
$cardOutputDetails->{HolderName};
$cardOutputDetails->{IIN};
$cardOutputDetails->{Last4};
$cardOutputDetails->{NumberLength};
$cardOutputDetails->{MaskedNumber};
$cardOutputDetails->{MaskedNumberAlternative};
$pspPaymentMethods0->{FingerPrint};

my $person = $pspPaymentMethods0->{Person};
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

my $address = $pspPaymentMethods0->{Address};
$address->{Street};
$address->{HouseNumber};
$address->{AdditionalInfo};
$address->{City};
$address->{StateProvince};
$address->{Country};
$address->{ZipCode};
$pspPaymentMethods0->{CreatedAt};
$pspPaymentMethods0->{UpdatedAt};

$response->{psp_PosDateTime};
