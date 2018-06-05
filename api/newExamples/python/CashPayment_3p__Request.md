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
    'psp_MerchTxRef': 'ORDER32145-3',
    'psp_MerchOrderId': 'ORDER32145',
    'psp_ReturnURL': 'http://localhost/',
    'psp_FrmLanguage': 'es_AR',
    'psp_Amount': '15050',
    'psp_Currency': '032',
    'psp_Country': 'ARG',
    'psp_Product': '301',
    'psp_PosDateTime': '2019-12-01 12:00:00',
    'psp_FirstExpDate': '2020-01-01'
}

try: 
    response = sdk.cash_payment_3p(params) 
except ApiException: 
    # Code to handle error 
    pass 
