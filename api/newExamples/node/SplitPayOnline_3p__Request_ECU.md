var Sdk = require('../lib/nps-sdk');
var constants = require('../lib/constants');
var sdk = new Sdk();

sdk.connect({environment: constants.SANDBOX_ENV,
            secretKey: 'YOUR_SECRET_KEY'});

sdk.splitPayOnline3p({
    'psp_Version': '2.2',
    'psp_MerchantId': 'psp_test',
    'psp_TxSource': 'WEB',
    'psp_MerchOrderId': 'ORDER66666',
    'psp_ReturnURL': 'http://localhost/',
    'psp_FrmLanguage': 'es_AR',
    'psp_Amount': '62400',
    'psp_Currency': '840',
    'psp_Country': 'ECU',
    'psp_Product': '14',
    'psp_PosDateTime': '2019-12-01 12:00:00',
    'psp_Transactions': [
        {
            'psp_MerchantId': 'psp_test',
            'psp_MerchTxRef': 'ORDER66666-3',
            'psp_Product': '14',
            'psp_Amount': '31200',
            'psp_NumPayments': '1',
            'psp_AmountAdditionalDetails': {
                'Taxes': [
                    {
                        'TypeId': '700',
                        'Amount': '1200',
                        'Rate': '1200',
                        'BaseAmount': '10000'
                    },
                    {
                        'TypeId': '701',
                        'BaseAmount': '20000'
                    }
                ]
                    }
        },
        {
            'psp_MerchantId': 'psp_test',
            'psp_MerchTxRef': 'ORDER66666-3',
            'psp_Product': '14',
            'psp_Amount': '31200',
            'psp_NumPayments': '1',
            'psp_AmountAdditionalDetails': {
                'Taxes': [
                    {
                        'TypeId': '700',
                        'Amount': '1200',
                        'Rate': '1200',
                        'BaseAmount': '10000'
                    },
                    {
                        'TypeId': '701',
                        'BaseAmount': '20000'
                    }
                ]
                    }
        },
    ]
},
function (error, response) { 
    if (error) {
        console.log(error)
    } else { 
        console.log(response)
    }
});

