import nps_sdk
from nps_sdk.constants import PRODUCTION_ENV, STAGING_ENV, SANDBOX_ENV
from nps_sdk.errors import ApiException

nps_sdk.Configuration.configure(environment=SANDBOX_ENV,
                            secret_key="_YOUR_SECRET_KEY_")
sdk = nps_sdk.Nps()

params = {
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
        'CardInputDetails': {
            'Number': '4507990000000010',
            'ExpirationDate': '2501',
            'SecurityCode': '123',
            'HolderName': 'JOHN DOE'
            },
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
}

try: 
    response = sdk.create_customer(params) 
except ApiException: 
    # Code to handle error 
    pass 
