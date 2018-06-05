import nps_sdk
from nps_sdk.constants import PRODUCTION_ENV, STAGING_ENV, SANDBOX_ENV
from nps_sdk.errors import ApiException

nps_sdk.Configuration.configure(environment=SANDBOX_ENV,
                            secret_key="_YOUR_SECRET_KEY_")
sdk = nps_sdk.Nps()

params = {
    'psp_Version': '2.2',
    'psp_MerchantId': 'sdk_test',
    'psp_CustomerId': 'bMnVPbNgX55oUz1VLgC41E5iD2rYRo2b',
    'psp_EmailAddress': 'jhon.doe@example.com',
    'psp_AlternativeEmailAddress': 'jdoe@example.com',
    'psp_AccountCreatedAt': '2010-10-23',
    'psp_AccountID': 'jdoe78',
    'psp_Person': {
        'FirstName': 'John',
        'LastName': 'Doe',
        'MiddleName': 'Michael',
        'PhoneNumber1': '+1 011 11111111',
        'PhoneNumber2': '+1 011 22222222',
        'Gender': 'M',
        'DateOfBirth': '1979-01-12',
        'Nationality': 'ARG',
        'IDNumber': '54111111',
        'IDType': '200'
    },
    'psp_Address': {
        'Street': 'Av. Collins',
        'HouseNumber': '1245',
        'AdditionalInfo': '2 A',
        'City': 'Miami',
        'StateProvince': 'Florida',
        'Country': 'USA',
        'ZipCode': '33140'
    },
    'psp_PaymentMethod': {
        'PaymentMethodToken': 'vp1PTJuKCVMXsbeOoAx94gxv2dQM5fUK',
        'Person': {
            'FirstName': 'John',
            'LastName': 'Doe',
            'MiddleName': 'Michael',
            'PhoneNumber1': '+1 011 11111111',
            'PhoneNumber2': '+1 011 22222222',
            'Gender': 'M',
            'DateOfBirth': '1979-01-12',
            'Nationality': 'ARG',
            'IDNumber': '54111111',
            'IDType': '200'
            },
        'Address': {
            'Street': 'Av. Collins',
            'HouseNumber': '1245',
            'AdditionalInfo': '2 A',
            'City': 'Miami',
            'StateProvince': 'Florida',
            'Country': 'USA',
            'ZipCode': '33140'
            }
    },
    'psp_PosDateTime': '2008-01-12 13:05:00'
}

try: 
    response = sdk.update_customer(params) 
except ApiException: 
    # Code to handle error 
    pass 
