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
    'psp_MerchOrderId': 'ORDER66666',
    'psp_ReturnURL': 'http://localhost/',
    'psp_FrmLanguage': 'es_AR',
    'psp_Amount': '15050',
    'psp_Currency': '032',
    'psp_Country': 'ARG',
    'psp_Product': '14',
    'psp_PosDateTime': '2019-12-01 12:00:00',
    'psp_Transactions': [
        {
            'psp_MerchantId': 'sdk_test',
            'psp_MerchTxRef': 'ORDER66666-3',
            'psp_Product': '14',
            'psp_Amount': '10000',
            'psp_NumPayments': '1'
        },
        {
            'psp_MerchantId': 'psp_test',
            'psp_MerchTxRef': 'ORDER66666-3',
            'psp_Product': '14',
            'psp_Amount': '5050',
            'psp_NumPayments': '12'
        }
    ]
}

try: 
    response = sdk.split_pay_online_3p(params) 
except ApiException: 
    # Code to handle error 
    pass 
