import nps_sdk
from nps_sdk.constants import PRODUCTION_ENV, STAGING_ENV, SANDBOX_ENV
from nps_sdk.errors import ApiException

nps_sdk.Configuration.configure(environment=SANDBOX_ENV,
                            secret_key="_YOUR_SECRET_KEY_")
sdk = nps_sdk.Nps()

params = {
    'psp_Version': '2.2',
    'psp_MerchantId': 'sdk_test',
    'psp_TransactionId': '65340022',
    'psp_PaymentMethodTag': 'Corporate card',
    'psp_CustomerId': 'bMnVPbNgX55oUz1VLgC41E5iD2rYRo2b',
    'psp_SetAsCustomerDefault': '1',
    'psp_PosDateTime': '2008-01-12 13:05:00'
}

try: 
    response = sdk.create_payment_method_from_payment(params) 
except ApiException: 
    # Code to handle error 
    pass 
