NPS.setMerchantId("sdk_test")
NPS.setClientSession("YOUR_CLIENT_SESSION")

PaymentMethodTokenParams = {
    card: {
        holder_name: "John Smith",
        number: "4507990000000010",
        exp_month: "01",
        exp_year: "2019",
        security_code: "123",
    },
    billing: {
        person: {
            firstname: "John",
            middlename: "Jay",
            lastname: "Smith",
            phonenumber1: "4123-1234",
            phonenumber2: "4123-1234",
            gender: "M",
            birthday: "1987-01-01",
            nationality: "ARG",
            idtype: "500",
            idnumber: "500"
      },
        address: {
            street: "Fakestreet",
            housenumber: "999",
            city: "Fakecity",
            country: "ARG",
            zip: "1234",
            state: "Fakestate",
            addinfo: "Fakeinfo",
      }
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