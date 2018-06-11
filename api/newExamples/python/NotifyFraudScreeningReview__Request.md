import nps_sdk
from nps_sdk.constants import PRODUCTION_ENV, STAGING_ENV, SANDBOX_ENV
from nps_sdk.errors import ApiException

nps_sdk.Configuration.configure(environment=SANDBOX_ENV,
                            secret_key="_YOUR_SECRET_KEY_")
sdk = nps_sdk.Nps()

params = {
    'psp_Version': '2.2',
    'psp_MerchantId': 'sdk_test',
    'psp_Criteria': 'T',
    'psp_CriteriaId': 'ORDER69461-3',
    'psp_ReviewResult': 'A',
    'psp_PosDateTime': '2019-12-01 12:00:00'
}

try: 
    response = sdk.notify_fraud_screening_review(params) 
except ApiException: 
    # Code to handle error 
    pass 
