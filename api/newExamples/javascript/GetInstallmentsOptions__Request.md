NPS.setClientSession('__YOUR_NPS_CLIENT_SESSION__');
NPS.setMerchantId('sdk_test');

NPS.setAmount('120000');
NPS.setCountry('CHL');
NPS.setCurrency('152');

var psp_PaymentMethodToken = '73vK7lLHGUtd2OGNCDfHtqQItBadjfGV';
var psp_Product = '14';
var psp_NumPayments = '3';

var response = NPS.card.getInstallmentsOptions(psp_PaymentMethodToken, psp_Product, psp_NumPayments);

