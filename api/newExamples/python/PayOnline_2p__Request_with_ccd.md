import nps_sdk
from nps_sdk.constants import PRODUCTION_ENV, STAGING_ENV, SANDBOX_ENV
from nps_sdk.errors import ApiException

nps_sdk.Configuration.configure(environment=SANDBOX_ENV,
                            secret_key="_YOUR_SECRET_KEY_")
sdk = nps_sdk.Nps()

params = {
    'psp_Version': '2.2',
    'psp_MerchantId': 'sdk_test',
    'psp_TxSource': 'WEB',
    'psp_MerchTxRef': 'ORDERX1466Xz-3',
    'psp_MerchOrderId': 'ORDERX1466Xz',
    'psp_Amount': '15050',
    'psp_NumPayments': '1',
    'psp_Currency': '032',
    'psp_Country': 'ARG',
    'psp_Product': '14',
    'psp_CardNumber': '4507990000000010',
    'psp_CardExpDate': '1912',
    'psp_PosDateTime': '2019-12-01 12:00:00',
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
    }
}

try: 
    response = sdk.pay_online_2p(params) 
except ApiException: 
    # Code to handle error 
    pass 
