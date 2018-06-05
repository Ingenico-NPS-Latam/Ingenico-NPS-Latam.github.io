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
    'psp_ReturnURL': 'http://localhost/',
    'psp_FrmLanguage': 'es_AR',
    'psp_ScreenDescription': 'Descripcion',
    'psp_TicketDescription': 'Descripcion',
    'psp_Currency': '032',
    'psp_Country': 'ARG',
    'psp_Product': '320',
    'psp_ExpDate1': '2019-12-01',
    'psp_Amount1': '15050',
    'psp_ExpMark': '0',
    'psp_ExpTime': '14:00:00',
    'psp_PosDateTime': '2019-12-01 12:00:00'
}

try: 
    response = sdk.bank_payment_3p(params) 
except ApiException: 
    # Code to handle error 
    pass 
