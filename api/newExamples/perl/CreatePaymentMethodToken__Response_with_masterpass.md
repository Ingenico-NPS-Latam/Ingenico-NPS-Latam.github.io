use NpsSDK::Nps;
use warnings;
use strict;

my $response = NpsSDK::Nps::create_payment_method_token($params);

$response->{psp_ResponseCod};
$response->{psp_ResponseMsg};
$response->{psp_MerchantId};
$response->{psp_PaymentMethodToken};
$response->{psp_Product};

my $pspWalletOutputDetails = $response->{psp_WalletOutputDetails};

my $cardOutputDetails = $pspWalletOutputDetails->{CardOutputDetails};
$cardOutputDetails->{ExpirationDate};
$cardOutputDetails->{ExpirationYear};
$cardOutputDetails->{ExpirationMonth};
$cardOutputDetails->{HolderName};
$cardOutputDetails->{IIN};
$cardOutputDetails->{Last4};
$cardOutputDetails->{NumberLength};
$cardOutputDetails->{MaskedNumber};
$cardOutputDetails->{MaskedNumberAlternative};

my $shippingDetails = $pspWalletOutputDetails->{ShippingDetails};
$shippingDetails->{Method};

my $primaryRecipient = $shippingDetails->{PrimaryRecipient};
$primaryRecipient->{FirstName};
$primaryRecipient->{PhoneNumber1};

my $address = $shippingDetails->{Address};
$address->{Street};

my $houseNumber = $address->{HouseNumber};
$address->{AdditionalInfo};
$address->{City};
$address->{Country};
$address->{ZipCode};

my $pspAddress = $response->{psp_Address};
$pspAddress->{Street};
$pspAddress->{AdditionalInfo};
$pspAddress->{City};
$pspAddress->{Country};
$pspAddress->{ZipCode};
$response->{psp_AlreadyUsed};
$response->{psp_CreatedAt};
$response->{psp_UpdatedAt};
