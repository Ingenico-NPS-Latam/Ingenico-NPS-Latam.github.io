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
    'psp_MerchOrderId': 'ORDER66666',
    'psp_Amount': '15050',
    'psp_NumPayments': '1',
    'psp_Currency': '032',
    'psp_Country': 'ARG',
    'psp_Product': '14',
    'psp_CardNumber': '4507990000000010',
    'psp_CardExpDate': '1912',
    'psp_PosDateTime': '2019-12-01 12:00:00',
    'psp_CustomerAdditionalDetails': {
        'DeviceFingerPrint': 'KJhKHKJgh7777kgh...'
    }
}

try: 
    response = sdk.fraud_screening(params) 
except ApiException: 
    # Code to handle error 
    pass 
