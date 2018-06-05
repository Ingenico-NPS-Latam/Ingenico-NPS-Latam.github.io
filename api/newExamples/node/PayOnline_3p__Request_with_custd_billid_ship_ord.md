var Sdk = require('../lib/nps-sdk');
var constants = require('../lib/constants');
var sdk = new Sdk();

sdk.connect({environment: constants.SANDBOX_ENV,
            secretKey: 'YOUR_SECRET_KEY'});

sdk.payOnline3p({
    'psp_Version': '2.2',
    'psp_MerchantId': 'sdk_test',
    'psp_TxSource': 'WEB',
    'psp_MerchTxRef': 'ORDER76666-3',
    'psp_MerchOrderId': 'ORDER76666',
    'psp_ReturnURL': 'http://localhost/',
    'psp_FrmLanguage': 'es_AR',
    'psp_Amount': '15050',
    'psp_NumPayments': '1',
    'psp_Currency': '032',
    'psp_Country': 'ARG',
    'psp_Product': '14',
    'psp_PosDateTime': '2019-12-01 12:00:00',
    'psp_CustomerAdditionalDetails': {
        'EmailAddress': 'jdoe@email.com',
        'AlternativeEmailAddress': 'Jdoe79@email.com',
        'IPAddress': '192.168.158.190',
        'AccountID': 'Jdoe78',
        'AccountCreatedAt': '2010-10-23',
        'AccountPreviousActivity': '1',
        'AccountHasCredentials': '1',
        'DeviceType': '1',
        'DeviceFingerPrint': 'KJhKHKJgh7777kgh...',
        'BrowserLanguage': 'ES',
        'HttpUserAgent': 'Mozilla/5.0 (X11; Ubuntu; Linux x86_64; rv:21.0) Gecko/20100101 Firefox/21.0'
    },
    'psp_BillingDetails': {
        'Invoice': '54877555',
        'InvoiceDate': '2017-10-23',
        'InvoiceAmount': '15050',
        'InvoiceCurrency': '032',
        'Person': {
            'DateOfBirth': '1979-01-12',
            'FirstName': 'John',
            'Gender': 'M',
            'IDNumber': '54111111',
            'IDType': '200',
            'LastName': 'Doe',
            'MiddleName': 'Michael',
            'Nationality': 'ARG',
            'PhoneNumber1': '+1 011 11111111',
            'PhoneNumber2': '+1 011 22222222'
            },
        'Address': {
            'AdditionalInfo': '2 A',
            'City': 'Miami',
            'Country': 'USA',
            'HouseNumber': '1245',
            'StateProvince': 'Florida',
            'Street': 'Av. Collins',
            'ZipCode': '33140'
            }
    },
    'psp_ShippingDetails': {
        'TrackingNumber': '154DDD54DWW11',
        'Method': '10',
        'Carrier': '200',
        'DeliveryDate': '2014-11-20',
        'FreightAmount': '15000',
        'GiftMessage': 'Happy Birthday!',
        'GiftWrapping': '1',
        'PrimaryRecipient': {
            'DateOfBirth': '1979-01-12',
            'FirstName': 'John',
            'Gender': 'M',
            'IDNumber': '54111111',
            'IDType': '200',
            'LastName': 'Doe',
            'MiddleName': 'Michael',
            'Nationality': 'ARG',
            'PhoneNumber1': '+1 011 11111111',
            'PhoneNumber2': '+1 011 22222222'
            },
        'SecondaryRecipient': {
            'DateOfBirth': '1979-01-12',
            'FirstName': 'John',
            'Gender': 'M',
            'IDNumber': '54111111',
            'IDType': '200',
            'LastName': 'Doe',
            'MiddleName': 'Michael',
            'Nationality': 'ARG',
            'PhoneNumber1': '+1 011 11111111',
            'PhoneNumber2': '+1 011 22222222'
            },
        'Address': {
            'AdditionalInfo': '2 A',
            'City': 'Miami',
            'Country': 'USA',
            'HouseNumber': '1245',
            'StateProvince': 'Florida',
            'Street': 'Av. Collins',
            'ZipCode': '33140'
            }
    },
    'psp_OrderDetails': {
        'OrderItems': [
            {
                'Quantity': '10',
                'UnitPrice': '10050',
                'Description': 'Blue pencil',
                'Type': '1002',
                'SkuCode': 'SO-4587885545',
                'ManufacturerPartNumber': 'CN-0N2828421-3AD-02CD',
                'Risk': 'H'
            }
        ]
    }
},
function (error, response) { 
    if (error) {
        console.log(error)
    } else { 
        console.log(response)
    }
});

