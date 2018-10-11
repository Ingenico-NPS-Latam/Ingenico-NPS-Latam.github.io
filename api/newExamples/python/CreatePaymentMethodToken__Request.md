import nps_sdk
from nps_sdk.constants import PRODUCTION_ENV, STAGING_ENV, SANDBOX_ENV
from nps_sdk.errors import ApiException

nps_sdk.Configuration.configure(environment=SANDBOX_ENV,
                            secret_key="_YOUR_SECRET_KEY_")
sdk = nps_sdk.Nps()

params = {
    'psp_Version': '2.2',
    'psp_MerchantId': 'sdk_test',
    'psp_WalletInputDetails': {
        'WalletTypeId': '2',
        'WalletKey': '3688e6474192fbaaca6f46f96142b82509c87000',
        'MerchOrderId': '1efed583-1824-436a-869f-286ebdb22ae9'
    },
    'psp_ClientSession': 'C5jwwbyAYneLbvZe0IYPHTvn7ODMb3vG8ZqCYaYIioUmWUbcgKscGpg8WhXrspRs'
}

try: 
    response = sdk.create_payment_method_token(params) 
except ApiException: 
    # Code to handle error 
    pass 
