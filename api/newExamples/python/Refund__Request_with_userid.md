import nps_sdk
from nps_sdk.constants import PRODUCTION_ENV, STAGING_ENV, SANDBOX_ENV
from nps_sdk.errors import ApiException

nps_sdk.Configuration.configure(environment=SANDBOX_ENV,
                            secret_key="_YOUR_SECRET_KEY_")
sdk = nps_sdk.Nps()

params = {
    'psp_Version': '2.2',
    'psp_MerchantId': 'sdk_test',
    'psp_TxSource': 'WEB',
    'psp_MerchTxRef': 'ORDER66666-3',
    'psp_TransactionId_Orig': '2693348',
    'psp_AmountToRefund': '15050',
    'psp_UserId': 'john_doe',
    'psp_PosDateTime': '2019-12-01 12:00:00'
}

try: 
    response = sdk.refund(params) 
except ApiException: 
    # Code to handle error 
    pass 
