import nps_sdk
from nps_sdk.constants import PRODUCTION_ENV, STAGING_ENV, SANDBOX_ENV
from nps_sdk.errors import ApiException

nps_sdk.Configuration.configure(environment=SANDBOX_ENV,
                            secret_key="_YOUR_SECRET_KEY_")
sdk = nps_sdk.Nps()

params = {
    'psp_Version': '2.2',
    'psp_MerchantId': 'sdk_test',
    'psp_EmailAddress': 'jhon.doe@example.com',
    'psp_AlternativeEmailAddress': 'jdoe@example.com',
    'psp_AccountID': 'jdoe78',
    'psp_AccountCreatedAt': '2010-10-23',
    'psp_PaymentMethod': {
        'PaymentMethodToken': 'KCVMXsbue5fUKOoAxvp1PTJ94gxv2dQM'
    },
    'psp_PosDateTime': '2008-01-12 13:05:00'
}

try: 
    response = sdk.create_customer(params) 
except ApiException: 
    # Code to handle error 
    pass 
