import nps_sdk
from nps_sdk.constants import PRODUCTION_ENV, STAGING_ENV, SANDBOX_ENV
from nps_sdk.errors import ApiException

nps_sdk.Configuration.configure(environment=SANDBOX_ENV,
                            secret_key="_YOUR_SECRET_KEY_")
sdk = nps_sdk.Nps()

params = {
    'psp_Version': '2.2',
    'psp_MerchantId': 'sdk_test',
    'psp_PaymentMethodId': 'jGW24iDaoMBzfKHViL18TmHo9sHBgW4J',
    'psp_PosDateTime': '2008-01-12 13:05:00'
}

try: 
    response = sdk.retrieve_payment_method(params) 
except ApiException: 
    # Code to handle error 
    pass 
