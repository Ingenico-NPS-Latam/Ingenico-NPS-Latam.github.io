var Sdk = require('../lib/nps-sdk');
var constants = require('../lib/constants');
var sdk = new Sdk();

sdk.connect({environment: constants.SANDBOX_ENV,
            secretKey: 'YOUR_SECRET_KEY'});

sdk.createPaymentMethodToken({
    'psp_Version': '2.2',
    'psp_MerchantId': 'sdk_test',
    'psp_CardInputDetails': {
        'Number': '4507990000000010',
        'ExpirationDate': '2501',
        'SecurityCode': '123',
        'HolderName': 'JOHN DOE'
    },
    'psp_ClientSession': 'C5jwwbyAYneLbvZe0IYPHTvn7ODMb3vG8ZqCYaYIioUmWUbcgKscGpg8WhXrspRs'
},
function (error, response) { 
    if (error) {
        console.log(error)
    } else { 
        console.log(response)
    }
});

