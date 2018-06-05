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
    'psp_MerchTxRef': 'ORDERX1466Xz-3',
    'psp_MerchOrderId': 'ORDERX1466Xz',
    'psp_Amount': '1220000',
    'psp_NumPayments': '1',
    'psp_Currency': '858',
    'psp_Country': 'URY',
    'psp_Product': '5',
    'psp_CardNumber': '5453010000083303',
    'psp_CardExpDate': '1904',
    'psp_PosDateTime': '2019-12-01 12:00:00',
    'psp_AmountAdditionalDetails': {
        'Tip': '20',
        'Discount': '1',
        'Taxes': [
            {
                'TypeId': '601',
                'Amount': '220000',
                'Rate': '2200',
                'BaseAmount': '1000000'
            }
        ]
    },
    'psp_BillingDetails': {
        'Invoice': 'A00024144',
        'InvoiceAmount': '1600000',
        'InvoiceCurrency': '858'
    }
}

try: 
    response = sdk.pay_online_2p(params) 
except ApiException: 
    # Code to handle error 
    pass 
