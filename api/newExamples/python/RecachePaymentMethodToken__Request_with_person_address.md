import nps_sdk
from nps_sdk.constants import PRODUCTION_ENV, STAGING_ENV, SANDBOX_ENV
from nps_sdk.errors import ApiException

nps_sdk.Configuration.configure(environment=SANDBOX_ENV,
                            secret_key="_YOUR_SECRET_KEY_")
sdk = nps_sdk.Nps()

params = {
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
}

try: 
    response = sdk.recache_payment_method_token(params) 
except ApiException: 
    # Code to handle error 
    pass 
