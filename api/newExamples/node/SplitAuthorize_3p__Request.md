var Sdk = require('../lib/nps-sdk');
var constants = require('../lib/constants');
var sdk = new Sdk();

sdk.connect({environment: constants.SANDBOX_ENV,
            secretKey: 'YOUR_SECRET_KEY'});

sdk.splitAuthorize3p({
    'psp_Version': '2.2',
    'psp_MerchantId': 'sdk_test',
    'psp_TxSource': 'WEB',
    'psp_MerchOrderId': 'ORDER66666',
    'psp_ReturnURL': 'http://localhost/',
    'psp_FrmLanguage': 'es_AR',
    'psp_Amount': '15050',
    'psp_Currency': '032',
    'psp_Country': 'ARG',
    'psp_Product': '14',
    'psp_PosDateTime': '2019-12-01 12:00:00',
    'psp_Transactions': [
        {
            'psp_MerchantId': 'sdk_test',
            'psp_MerchTxRef': 'ORDER66666-3',
            'psp_Product': '14',
            'psp_Amount': '10000',
            'psp_NumPayments': '1'
        },
        {
            'psp_MerchantId': 'sdk_test',
            'psp_MerchTxRef': 'ORDER66666-3',
            'psp_Product': '14',
            'psp_Amount': '5050',
            'psp_NumPayments': '1'
        }
    ]
},
function (error, response) { 
    if (error) {
        console.log(error)
    } else { 
        console.log(response)
    }
});

