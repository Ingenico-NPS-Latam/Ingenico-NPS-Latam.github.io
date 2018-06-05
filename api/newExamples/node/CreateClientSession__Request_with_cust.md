var Sdk = require('../lib/nps-sdk');
var constants = require('../lib/constants');
var sdk = new Sdk();

sdk.connect({environment: constants.SANDBOX_ENV,
            secretKey: 'YOUR_SECRET_KEY'});

sdk.createClientSession({
    'psp_Version': '2.2',
    'psp_MerchantId': 'sdk_test',
    'psp_PosDateTime': '2019-12-01 12:00:00',
    'psp_CustomerId': 'K8sj5rBrGqPBczTR4LtuKE6g4iZMmY9f'
},
function (error, response) { 
    if (error) {
        console.log(error)
    } else { 
        console.log(response)
    }
});

