var Sdk = require('../lib/nps-sdk');
var constants = require('../lib/constants');
var sdk = new Sdk();

sdk.connect({environment: constants.SANDBOX_ENV,
            secretKey: 'YOUR_SECRET_KEY'});

sdk.createPaymentMethod({
    'psp_Version': '2.2',
    'psp_MerchantId': 'sdk_test',
    'psp_PaymentMethod': {
        'PaymentMethodToken': 'HGIYeXKJpQyBvO3pHuZTN9JZiVPnzQaQ',
        'PaymentMethodTag': 'Corporate card',
        'Person': {
            'FirstName': 'John',
            'LastName': 'Doe',
            'MiddleName': 'Michael',
            'PhoneNumber1': '+1 011 11111111',
            'PhoneNumber2': '+1 011 22222222',
            'DateOfBirth': '1979-01-12',
            'Gender': 'M',
            'Nationality': 'ARG',
            'IDNumber': '54111111',
            'IDType': '200'
            },
        'Address': {
            'Street': 'Av. Collins',
            'HouseNumber': '4702',
            'AdditionalInfo': '2 A',
            'City': 'Buenos Aires',
            'StateProvince': 'CABA',
            'Country': 'ARG',
            'ZipCode': '1425'
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

