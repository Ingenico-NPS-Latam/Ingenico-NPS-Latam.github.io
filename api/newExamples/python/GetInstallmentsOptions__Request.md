import nps_sdk
from nps_sdk.constants import PRODUCTION_ENV, STAGING_ENV, SANDBOX_ENV
from nps_sdk.errors import ApiException

nps_sdk.Configuration.configure(environment=SANDBOX_ENV,
                            secret_key="_YOUR_SECRET_KEY_")
sdk = nps_sdk.Nps()

params = {
    'psp_Version': '2.2',
    'psp_MerchantId': 'sdk_test',
    'psp_Amount': '100',
    'psp_Product': '14',
    'psp_Currency': '152',
    'psp_Country': 'CHL',
    'psp_NumPayments': '1',
    'psp_PaymentMethodToken': 'KCVMXsbue5fUKOoAxvp1PTJ94gxv2dQM',
    'psp_ClientSession': 'C5jwwbyAYneLbvZe0IYPHTvn7ODMb3vG8ZqCYaYIioUmWUbcgKscGpg8WhXrspRs',
    'psp_PosDateTime': '2017-04-04 13:35:20'
}

try: 
    response = sdk.get_installments_options(params) 
except ApiException: 
    # Code to handle error 
    pass 
