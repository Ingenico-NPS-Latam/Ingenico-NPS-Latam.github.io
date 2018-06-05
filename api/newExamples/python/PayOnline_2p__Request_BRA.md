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
    'psp_MerchTxRef': 'ORDER69461-3',
    'psp_MerchOrderId': 'ORDER69461',
    'psp_Amount': '1200000',
    'psp_NumPayments': '1',
    'psp_Currency': '986',
    'psp_Country': 'BRA',
    'psp_Product': '14',
    'psp_CardNumber': '4507990000000010',
    'psp_CardExpDate': '1912',
    'psp_CardSecurityCode': '325',
    'psp_PosDateTime': '2019-12-01 12:00:00',
    'psp_AmountAdditionalDetails': {
        'Tip': '20',
        'Discount': '1',
        'Taxes': [
            {
                'TypeId': '100',
                'Amount': '200000'
            }
        ]
    }
}

try: 
    response = sdk.pay_online_2p(params) 
except ApiException: 
    # Code to handle error 
    pass 
