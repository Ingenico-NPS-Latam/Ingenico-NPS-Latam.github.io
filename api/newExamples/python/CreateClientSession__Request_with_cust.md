import nps_sdk
from nps_sdk.constants import PRODUCTION_ENV, STAGING_ENV, SANDBOX_ENV
from nps_sdk.errors import ApiException

nps_sdk.Configuration.configure(environment=SANDBOX_ENV,
                            secret_key="_YOUR_SECRET_KEY_")
sdk = nps_sdk.Nps()

params = {
    'psp_Version': '2.2',
    'psp_MerchantId': 'sdk_test',
    'psp_PosDateTime': '2019-12-01 12:00:00',
    'psp_CustomerId': 'K8sj5rBrGqPBczTR4LtuKE6g4iZMmY9f'
}

try: 
    response = sdk.create_client_session(params) 
except ApiException: 
    # Code to handle error 
    pass 
