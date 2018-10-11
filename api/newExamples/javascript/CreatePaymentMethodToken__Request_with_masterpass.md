NPS.setMerchantId("sdk_test")
NPS.setClientSession("YOUR_CLIENT_SESSION")

PaymentMethodTokenParams = {
    wallet: {
        type_id: "2",
        key: "d084703513e87cd1540a114cd7317e6642eca04e",
        orderId: "1efed583-1824-436a-869f-286ebdb22ae9",
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