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
    'psp_Person': {
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
    'psp_Address': {
        'Street': 'Av. Collins',
        'HouseNumber': '1245',
        'AdditionalInfo': '2 A',
        'StateProvince': 'Florida',
        'City': 'Miami',
        'Country': 'USA',
        'ZipCode': '33140'
    },
    'psp_PaymentMethod': {
        'PaymentMethodToken': 'KCVMXsbue5fUKOoAxvp1PTJ94gxv2dQM',
        'Address': {
            'Street': 'Av. Collins',
            'HouseNumber': '1245',
            'AdditionalInfo': '2 A',
            'StateProvince': 'Florida',
            'City': 'Miami',
            'Country': 'USA',
            'ZipCode': '33140'
            },
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

