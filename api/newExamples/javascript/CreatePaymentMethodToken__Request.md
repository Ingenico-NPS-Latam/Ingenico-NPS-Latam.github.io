NPS.setMerchantId("sdk_test")
NPS.setClientSession("YOUR_CLIENT_SESSION")

PaymentMethodTokenParams = {
    card: {
        holder_name: "John Smith",
        number: "4507990000000010",
        exp_month: "01",
        exp_year: "2019",
        security_code: "123",
    }    
};

var npsSuccessResponseHandler;
npsSuccessResponseHandler = function (paymentMethodToken) {
    //Code to handle success
};

var npsErrorResponseHandler;
npsErrorResponseHandler = function (response) {
    //Code to handle error
};


NPS.paymentMethodToken.create(PaymentMethodTokenParams, npsSuccessResponseHandler, npsErrorResponseHandler)