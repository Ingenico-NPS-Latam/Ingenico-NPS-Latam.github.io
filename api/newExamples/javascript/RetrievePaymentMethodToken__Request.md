NPS.setMerchantId('sdk_test');
NPS.setClientSession('YOUR_CLIENT_SESSION');

var paymentMethodTokenId = "p8hbRZ46KvgVqX22sqnxgDRCsdfNFEQq"

var npsSuccessResponseHandler;
npsSuccessResponseHandler = function (paymentMethodToken) {
    //Code to handle success
};

var npsErrorResponseHandler;
npsErrorResponseHandler = function (response) {
    //Code to handle error
};

NPS.paymentMethodToken.retrieve(paymentMethodTokenId, npsSuccessResponseHandler,npsErrorResponseHandler);