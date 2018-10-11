var Sdk = require('../lib/nps-sdk');
var constants = require('../lib/constants');
var sdk = new Sdk();

sdk.connect({environment: constants.SANDBOX_ENV,
            secretKey: 'YOUR_SECRET_KEY'});

sdk.createPaymentMethodToken({
    'psp_Version': '2.2',
    'psp_MerchantId': 'sdk_test',
    'psp_WalletInputDetails': {
        'WalletTypeId': '2',
        'WalletKey': 'd084703513e87cd1540a114cd7317e6642eca04e',
        'MerchOrderId': '1efed583-1824-436a-869f-286ebdb22ae9'
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

