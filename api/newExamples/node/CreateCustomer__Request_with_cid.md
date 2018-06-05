var Sdk = require('../lib/nps-sdk');
var constants = require('../lib/constants');
var sdk = new Sdk();

sdk.connect({environment: constants.SANDBOX_ENV,
            secretKey: 'YOUR_SECRET_KEY'});

sdk.createCustomer({
    'psp_Version': '2.2',
    'psp_MerchantId': 'sdk_test',
    'psp_EmailAddress': 'jhon.doe@example.com',
    'psp_AlternativeEmailAddress': 'jdoe@example.com',
    'psp_AccountID': 'jdoe78',
    'psp_AccountCreatedAt': '2010-10-23',
    'psp_PaymentMethod': {
        'CardInputDetails': {
            'Number': '4507990000000010',
            'ExpirationDate': '2501',
            'SecurityCode': '123',
            'HolderName': 'JOHN DOE'
            }
    },
    'psp_PosDateTime': '2008-01-12 13:05:00'
},
function (error, response) { 
    if (error) {
        console.log(error)
    } else { 
        console.log(response)
    }
});

