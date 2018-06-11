import nps_sdk
from nps_sdk.constants import PRODUCTION_ENV, STAGING_ENV, SANDBOX_ENV
from nps_sdk.errors import ApiException

nps_sdk.Configuration.configure(environment=SANDBOX_ENV,
                            secret_key="_YOUR_SECRET_KEY_")
sdk = nps_sdk.Nps()

params = {
    'psp_Version': '2.2',
    'psp_MerchantId': 'psp_test',
    'psp_TxSource': 'WEB',
    'psp_MerchTxRef': 'ORDER76666-3',
    'psp_MerchOrderId': 'ORDER76666',
    'psp_ReturnURL': 'http://localhost/',
    'psp_FrmLanguage': 'es_AR',
    'psp_NumPayments': '1',
    'psp_Currency': '840',
    'psp_Country': 'ECU',
    'psp_Product': '14',
    'psp_PosDateTime': '2019-12-01 12:00:00',
    'psp_Amount': '31200',
    'psp_AmountAdditionalDetails': {
        'Taxes': [
            {
                'TypeId': '700',
                'Amount': '1200',
                'Rate': '1200',
                'BaseAmount': '100000'
            },
            {
                'TypeId': '701',
                'BaseAmount': '20000'
            }
        ]
    }
}

try: 
    response = sdk.pay_online_3p(params) 
except ApiException: 
    # Code to handle error 
    pass 
