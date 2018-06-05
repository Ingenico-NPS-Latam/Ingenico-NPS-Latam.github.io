use NpsPerlSDK::Nps;
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

my $pspPerson = $response->{psp_Person};
$pspPerson->{FirstName};
$pspPerson->{LastName};
$pspPerson->{MiddleName};
$pspPerson->{PhoneNumber1};
$pspPerson->{PhoneNumber2};
$pspPerson->{Gender};
$pspPerson->{DateOfBirth};
$pspPerson->{Nationality};
$pspPerson->{IDNumber};
$pspPerson->{IDType};

my $pspAddress = $response->{psp_Address};
$pspAddress->{Street};
$pspAddress->{HouseNumber};
$pspAddress->{AdditionalInfo};
$pspAddress->{City};
$pspAddress->{StateProvince};
$pspAddress->{Country};
$pspAddress->{ZipCode};
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
$pspPaymentMethods0->{CreatedAt};
$pspPaymentMethods0->{UpdatedAt};

$response->{psp_PosDateTime};
