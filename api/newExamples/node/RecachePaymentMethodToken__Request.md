var Sdk = require('../lib/nps-sdk');
var constants = require('../lib/constants');
var sdk = new Sdk();

sdk.connect({environment: constants.SANDBOX_ENV,
            secretKey: 'YOUR_SECRET_KEY'});

sdk.recachePaymentMethodToken({
    'psp_Version': '2.2',
    'psp_MerchantId': 'sdk_test',
    'psp_PaymentMethodId': 'Nzmd7DyGytXXC5PtKwnCsXXuQWHJB9EE',
    'psp_CardSecurityCode': '123',
    'psp_ClientSession': 'C5jwwbyAYneLbvZe0IYPHTvn7ODMb3vG8ZqCYaYIioUmWUbcgKscGpg8WhXrspRs'
},
function (error, response) { 
    if (error) {
        console.log(error)
    } else { 
        console.log(response)
    }
});

