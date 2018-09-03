NPS.setMerchantId('sdk_test');
NPS.setClientSession('YOUR_CLIENT_SESSION');

PaymentMethodTokenParams = {
    card: {
        payment_method_id: 'gXnsNd7hhfIzAd9PkRov1MJeEVGlSKe7',
        security_code: '123',
    },
    billing: {
        person: {
            firstname: 'John',
            middlename: 'Jay',
            lastname: 'Smith',
            phonenumber1: '4123-1234',
            phonenumber2: '4123-1234',
            gender: 'M',
            birthday: '1987-01-01',
            nationality: 'ARG',
            idtype: '500',
            idnumber: '500'
        },
        address: {
            street: 'Fakestreet',
            housenumber: '999',
            city: 'Fakecity',
            country: 'ARG',
            zip: '1234',
            state: 'Fakestate',
            addinfo: 'Fakeinfo',
        }
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

