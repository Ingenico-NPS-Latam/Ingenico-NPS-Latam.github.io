use NpsPerlSDK::Nps;
use warnings;
use strict;

my $response = NpsSDK::Nps::recache_payment_method_token($params);

$response->{psp_ResponseCod};
$response->{psp_ResponseMsg};
$response->{psp_MerchantId};
$response->{psp_PaymentMethodToken};
$response->{psp_Product};

my $pspCardOutputDetails = $response->{psp_CardOutputDetails};
$pspCardOutputDetails->{ExpirationDate};
$pspCardOutputDetails->{ExpirationYear};
$pspCardOutputDetails->{ExpirationMonth};
$pspCardOutputDetails->{HolderName};
$pspCardOutputDetails->{IIN};
$pspCardOutputDetails->{Last4};
$pspCardOutputDetails->{NumberLength};
$pspCardOutputDetails->{MaskedNumber};
$pspCardOutputDetails->{MaskedNumberAlternative};

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
$response->{psp_AlreadyUsed};
$response->{psp_CreatedAt};
$response->{psp_UpdatedAt};
