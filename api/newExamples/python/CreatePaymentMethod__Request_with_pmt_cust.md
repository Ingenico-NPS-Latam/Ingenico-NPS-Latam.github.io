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
    'psp_SetAsCustomerDefault': '1',
    'psp_PosDateTime': '2008-01-12 13:05:00'
}

try: 
    response = sdk.create_payment_method(params) 
except ApiException: 
    # Code to handle error 
    pass 
