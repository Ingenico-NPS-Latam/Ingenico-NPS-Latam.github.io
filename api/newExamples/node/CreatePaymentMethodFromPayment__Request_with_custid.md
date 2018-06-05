var Sdk = require('../lib/nps-sdk');
var constants = require('../lib/constants');
var sdk = new Sdk();

sdk.connect({environment: constants.SANDBOX_ENV,
            secretKey: 'YOUR_SECRET_KEY'});

sdk.createPaymentMethodFromPayment({
    'psp_Version': '2.2',
    'psp_MerchantId': 'sdk_test',
    'psp_TransactionId': '65340022',
    'psp_PaymentMethodTag': 'Corporate card',
    'psp_CustomerId': 'bMnVPbNgX55oUz1VLgC41E5iD2rYRo2b',
    'psp_SetAsCustomerDefault': '1',
    'psp_PosDateTime': '2008-01-12 13:05:00'
},
function (error, response) { 
    if (error) {
        console.log(error)
    } else { 
        console.log(response)
    }
});

