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
    'psp_ClientSession': 'C5jwwbyAYneLbvZe0IYPHTvn7ODMb3vG8ZqCYaYIioUmWUbcgKscGpg8WhXrspRs'
}

try: 
    response = sdk.create_payment_method_token(params) 
except ApiException: 
    # Code to handle error 
    pass 
