var Sdk = require('../lib/nps-sdk');
var constants = require('../lib/constants');
var sdk = new Sdk();

sdk.connect({environment: constants.SANDBOX_ENV,
            secretKey: 'YOUR_SECRET_KEY'});

sdk.getInstallmentsOptions({
    'psp_Version': '2.2',
    'psp_MerchantId': 'sdk_test',
    'psp_Amount': '100',
    'psp_Product': '14',
    'psp_Currency': '152',
    'psp_Country': 'CHL',
    'psp_NumPayments': '12',
    'psp_PaymentMethodToken': 'KCVMXsbue5fUKOoAxvp1PTJ94gxv2dQM',
    'psp_ClientSession': 'C5jwwbyAYneLbvZe0IYPHTvn7ODMb3vG8ZqCYaYIioUmWUbcgKscGpg8WhXrspRs',
    'psp_PosDateTime': '2017-04-04 13:35:20'
},
function (error, response) { 
    if (error) {
        console.log(error)
    } else { 
        console.log(response)
    }
});

