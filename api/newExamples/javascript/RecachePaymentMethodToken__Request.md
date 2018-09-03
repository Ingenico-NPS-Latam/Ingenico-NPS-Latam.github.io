NPS.setMerchantId('sdk_test');
NPS.setClientSession('YOUR_CLIENT_SESSION');

PaymentMethodTokenParams = {
    card: {
        payment_method_id: 'gXnsNd7hhfIzAd9PkRov1MJeEVGlSKe7',
        security_code: '123',
    }
}


var npsSuccessResponseHandler;
npsSuccessResponseHandler = function(paymentMethodToken) {
  //Success code
};

var npsErrorResponseHandler;
npsErrorResponseHandler = function(response) {
  //Error handler code
};

NPS.paymentMethodToken.recache(PaymentMethodTokenParams, npsSuccessResponseHandler, npsErrorResponseHandler);

