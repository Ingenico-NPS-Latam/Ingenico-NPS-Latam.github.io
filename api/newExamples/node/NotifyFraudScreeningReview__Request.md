var Sdk = require('../lib/nps-sdk');
var constants = require('../lib/constants');
var sdk = new Sdk();

sdk.connect({environment: constants.SANDBOX_ENV,
            secretKey: 'YOUR_SECRET_KEY'});

sdk.notifyFraudScreeningReview({
    'psp_Version': '2.2',
    'psp_MerchantId': 'sdk_test',
    'psp_Criteria': 'T',
    'psp_CriteriaId': 'ORDER69461-3',
    'psp_ReviewResult': 'A',
    'psp_PosDateTime': '2019-12-01 12:00:00'
},
function (error, response) { 
    if (error) {
        console.log(error)
    } else { 
        console.log(response)
    }
});

