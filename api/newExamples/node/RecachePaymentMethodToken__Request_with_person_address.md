var Sdk = require('../lib/nps-sdk');
var constants = require('../lib/constants');
var sdk = new Sdk();

sdk.connect({environment: constants.SANDBOX_ENV,
            secretKey: 'YOUR_SECRET_KEY'});

sdk.recachePaymentMethodToken({
    'psp_Version': '2.2',
    'psp_MerchantId': 'sdk_test',
    'psp_PaymentMethodId': 'Nzmd7DyGytXXC5PtKwnCsXXuQWHJB9EE',
    'psp_CardSecurityCode': '123',
    'psp_Person': {
        'FirstName': 'John',
        'DateOfBirth': '1979-01-12',
        'LastName': 'Doe',
        'MiddleName': 'Michael',
        'PhoneNumber1': '+1 011 11111111',
        'PhoneNumber2': '+1 011 22222222',
        'Gender': 'M',
        'Nationality': 'ARG',
        'IDNumber': '54111111',
        'IDType': '200'
    },
    'psp_Address': {
        'Street': 'Av. Collins',
        'HouseNumber': '4702',
        'AdditionalInfo': '2 A',
        'City': 'Buenos Aires',
        'StateProvince': 'CABA',
        'Country': 'ARG',
        'ZipCode': '1425'
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

