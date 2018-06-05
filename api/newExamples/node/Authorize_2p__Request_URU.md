var Sdk = require('../lib/nps-sdk');
var constants = require('../lib/constants');
var sdk = new Sdk();

sdk.connect({environment: constants.SANDBOX_ENV,
            secretKey: 'YOUR_SECRET_KEY'});

sdk.authorize2p({
    'psp_Version': '2.2',
    'psp_MerchantId': 'sdk_test',
    'psp_TxSource': 'WEB',
    'psp_MerchTxRef': 'ORDERX1466Xz-3',
    'psp_MerchOrderId': 'ORDERX1466Xz',
    'psp_Amount': '1220000',
    'psp_NumPayments': '1',
    'psp_Currency': '858',
    'psp_Country': 'URY',
    'psp_Product': '5',
    'psp_CardNumber': '5453010000083303',
    'psp_CardExpDate': '1904',
    'psp_PosDateTime': '2019-12-01 12:00:00',
    'psp_AmountAdditionalDetails': {
        'Tip': '20',
        'Discount': '1',
        'Taxes': [
            {
                'TypeId': '601',
                'Amount': '220000',
                'Rate': '2200',
                'BaseAmount': '1000000'
            }
        ]
    },
    'psp_BillingDetails': {
        'Invoice': 'A00024144',
        'InvoiceAmount': '1600000',
        'InvoiceCurrency': '858'
    }
},
function (error, response) { 
    if (error) {
        console.log(error)
    } else { 
        console.log(response)
    }
});

