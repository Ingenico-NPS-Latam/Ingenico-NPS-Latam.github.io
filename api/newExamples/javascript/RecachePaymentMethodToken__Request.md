<script>
PaymentMethodTokenParams = {
      card: {
        payment_method_id: 'gXnsNd7hhfIzAd9PkRov1MJeEVGlSKe7',
        security_code: '123',
      }, 
      billing: { // optional
        person: { // optional
          firstname: 'John',  // mandatory
          middlename: 'Jay', // optional
          lastname: 'Smith', // optional
          phonenumber1: '4123-1234', // optional
          phonenumber2: '4123-1234', // optional
          gender: 'M', // optional
          birthday: '1987-01-01', // optional
          nationality: 'ARG', // optional
          idtype: '500', // optional
          idnumber: '500' // optional
        },
        address: { // optional
          street: 'Fakestreet', // mandatory
          housenumber: '999', // mandatory
          city: 'Fakecity', // mandatory
          country: 'ARG', // mandatory
          zip: '1234', // optional
          state: 'Fakestate', // optional
          addinfo: 'Fakeinfo', // optional
        }
      }
    }
};

NPS.paymentMethodToken.recache(PaymentMethodTokenParams, npsSuccessResponseHandler, npsErrorResponseHandler);
</script>