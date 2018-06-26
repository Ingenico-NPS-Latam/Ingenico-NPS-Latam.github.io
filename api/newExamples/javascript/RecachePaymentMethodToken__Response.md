var npsSuccessResponseHandler;
npsSuccessResponseHandler = function (paymentMethodToken) {
    console.log(paymentMethodToken)

    console.log(paymentMethodToken.id)
    console.log(paymentMethodToken.used)
    console.log(paymentMethodToken.object)
    console.log(paymentMethodToken.product)
    console.log(paymentMethodToken.created_at)
    console.log(paymentMethodToken.updated_at)

    console.log(paymentMethodToken.billing)
    console.log(paymentMethodToken.billing.address)
    console.log(paymentMethodToken.billing.address.addinfo)
    console.log(paymentMethodToken.billing.address.city)
    console.log(paymentMethodToken.billing.address.country)
    console.log(paymentMethodToken.billing.address.housenumber)
    console.log(paymentMethodToken.billing.address.state)
    console.log(paymentMethodToken.billing.address.street)
    console.log(paymentMethodToken.billing.address.zip)

    console.log(paymentMethodToken.billing.person)
    console.log(paymentMethodToken.billing.person.birthday)
    console.log(paymentMethodToken.billing.person.firstname)
    console.log(paymentMethodToken.billing.person.gender)
    console.log(paymentMethodToken.billing.person.idnumber)
    console.log(paymentMethodToken.billing.person.idtype)
    console.log(paymentMethodToken.billing.person.lastname)
    console.log(paymentMethodToken.billing.person.middlename)
    console.log(paymentMethodToken.billing.person.nationality)
    console.log(paymentMethodToken.billing.person.phonenumber1)
    console.log(paymentMethodToken.billing.person.phonenumber2)

    console.log(paymentMethodToken.card)
    console.log(paymentMethodToken.card.exp_date)
    console.log(paymentMethodToken.card.exp_month)
    console.log(paymentMethodToken.card.exp_year)
    console.log(paymentMethodToken.card.holder_name)
    console.log(paymentMethodToken.card.iin)
    console.log(paymentMethodToken.card.last4)
    console.log(paymentMethodToken.card.masked_number)
    console.log(paymentMethodToken.card.masked_number_alternative)
    console.log(paymentMethodToken.card.number_length)
};

var npsErrorResponseHandler;
npsErrorResponseHandler = function (response) {
    console.log(response)

    console.log(response.object)
    console.log(response.type)
    console.log(response.message)
    console.log(response.message_to_purchaser)
};

NPS.paymentMethodToken.recache(PaymentMethodTokenParams, npsSuccessResponseHandler, npsErrorResponseHandler);