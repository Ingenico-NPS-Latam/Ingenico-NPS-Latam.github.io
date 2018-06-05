import nps_sdk
from nps_sdk.constants import PRODUCTION_ENV, STAGING_ENV, SANDBOX_ENV
from nps_sdk.errors import ApiException

nps_sdk.Configuration.configure(environment=SANDBOX_ENV,
                            secret_key="_YOUR_SECRET_KEY_")
sdk = nps_sdk.Nps()

params = {
    'psp_Version': '2.2',
    'psp_MerchantId': 'sdk_test',
    'psp_CardInputDetails': {
        'Number': '4507990000000010',
        'ExpirationDate': '2501',
        'SecurityCode': '123',
        'HolderName': 'JOHN DOE'
    },
    'psp_Person': {
        'FirstName': 'John',
        'LastName': 'Doe',
        'MiddleName': 'Michael',
        'DateOfBirth': '1979-01-12',
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
}

try: 
    response = sdk.create_payment_method_token(params) 
except ApiException: 
    # Code to handle error 
    pass 
