ArrayOfQueryTxsTransactions = {
    'psp_ResponseCod': '2',
    'psp_ResponseMsg': 'Transaccion exitosa - Aprobada',
    'psp_ResponseExtended': 'Aprobada',
    'psp_TransactionId': '100022',
    'psp_MerchantId': 'sdk_test',
    'psp_TxSource': 'WEB',
    'psp_Operation': 'TC  Autorizacion',
    'psp_MerchTxRef': 'ORDER1000-1',
    'psp_MerchOrderId': 'ORDER1000',
    'psp_MerchAdditionalRef': 'ADDITIONAL-REF1234',
    'psp_Amount': '15050',
    'psp_NumPayments': '1',
    'psp_PaymentAmount': '10050',
    'psp_Currency': '032',
    'psp_Country': 'ARG',
    'psp_Product': '14',
    'psp_AuthorizationCode': '352123',
    'psp_BatchNro': '1254',
    'psp_SequenceNumber': '64564321654',
    'psp_TicketNumber': '1254',
    'psp_CardNumber_FSD': '125478',
    'psp_CardNumber_LFD': '0001',
    'psp_CardMask': '451423XXXXXX1452',
    'psp_CardHolderName': 'JOHN DOE',
    'psp_CustomerMail': 'client@client.com.ar',
    'psp_CustomerId': 'P123765',
    'psp_CustomerHttpUserAgent': ' Mozilla/5.0 (X11; Ubuntu; Linux x86_64; rv:21.0) Gecko/20100101 Firefox/21.0',
    'psp_CustomerIpAddress': '200.123.123.100',
    'psp_MerchantMail': 'merchant@merchant.com.ar',
    'psp_ClTrnId': '365258',
    'psp_ClExternalMerchant': '96878987',
    'psp_ClExternalTerminal': '14587986',
    'psp_ClResponseCod': '155',
    'psp_ClResponseMsg': '33140',
    'psp_PosDateTime': '2008-01-12 13:05:00',
    'psp_PurchaseDescription': 'Com. X Art 1555',
    'psp_SoftDescriptor': 'Compra Art 15',
    'psp_Plan': 'PlanZ',
    'psp_3dSecure_XID': 'MjY0MjAxNjA4MDIyMDUzMzYyNjU=',
    'psp_3dSecure_CAVV': 'AAABBYZ3N5Qhl3kBU3c3ELGUsMY=',
    'psp_3dSecure_Eci': '05',
    'psp_3dSecure_EciMsg': '',
    'psp_3dSecure_Secured': '1',
    'psp_3dSecure_ProtocolVersion': '2.1.0', 
    'psp_3dSecure_DirectoryServerTransactionId': 'c4e59ceb-a382-4d6a-bc87-385d591fa09d',
    'psp_CreatedAt': '2008-01-12 13:05:35-03:00',
    'psp_AmountAdditionalDetails': {
        'Tip': '20000',
        'Discount': '11000',
        'Taxes': [
            {
                'TypeId': '500',
                'Amount': '10000',
                'Rate': '2100',
                'BaseAmount': '10000'
            },
            {
                'TypeId': '500',
                'Amount': '10000',
                'Rate': '2100',
                'BaseAmount': '10000'
            },
        ]
    },
    'psp_FraudScreeningResult': {
        'ResultCode': 'A',
        'ResultDescription': 'ACCEPT',
        'AdditionalInfo': 'Information'
    },
    'psp_VerificationServicesResult': {
        'ResultCodeCardSecurityCode': 'M',
        'ResultCodeBillingAddress': 'M',
        'ResultCodeBillingAddressZipCode': 'M',
        'ResultCodeBillingPersonIDType': 'M',
        'ResultCodeBillingPersonIDNumber': 'M',
        'ResultCodeBillingPersonDateOfBirth': 'M',
        'ResultCodeBillingPersonName': 'M',
        'ResultCodeBillingPersonPhoneNumber1': 'M',
        'ResultCodeCustomerEmailAddress': 'M'
    },
    'psp_MerchantAdditionalDetails': {
        'Type': '2 A',
        'SellerDetails': {
            'IDNumber': '30706033471',
            'IDType': '205',
            'Name': 'Company S.A.',
            'Invoice': '54877555',
            'PurchaseDescription': 'Samsung 4K SUHD TV',
            'Address': {
                'AdditionalInfo': '2 A',
                'City': 'Miami',
                'Country': 'USA',
                'HouseNumber': '1245',
                'StateProvince': 'Florida',
                'Street': 'Av. Collins',
                'ZipCode': '33140'
                    },
            'MCC': '5732',
            'ChannelCode': '',
            'GeoCode': ''
            }
    },
    'psp_CustomerAdditionalDetails': {
        'EmailAddress': 'jdoe@email.com',
        'AlternativeEmailAddress': 'Jdoe79@email.com',
        'IPAddress': '192.168.158.190',
        'AccountID': 'Jdoe78',
        'AccountCreatedAt': '2010-10-23',
        'AccountPreviousActivity': '1',
        'AccountHasCredentials': '1',
        'DeviceType': '1',
        'DeviceFingerPrint': 'KJhKHKJgh7777kgh',
        'BrowserLanguage': 'ES',
        'HttpUserAgent': 'Mozilla/5.0 (X11; Ubuntu; Linux x86_64; rv:21.0) Gecko/20100101 Firefox/21.0'
    },
    'psp_BillingDetails': {
        'Invoice': '54877555',
        'InvoiceDate': '2017-10-23',
        'InvoiceAmount': '15050',
        'InvoiceCurrency': '032',
        'Person': {
            'DateOfBirth': '1979-01-12',
            'FirstName': 'John',
            'Gender': 'M',
            'IDNumber': '54111111',
            'IDType': '200',
            'LastName': 'Doe',
            'MiddleName': 'Michael',
            'Nationality': 'ARG',
            'PhoneNumber1': '+1 011 11111111',
            'PhoneNumber2': '+1 011 22222222'
            },
        'Address': {
            'AdditionalInfo': '2 A',
            'City': 'Miami',
            'Country': 'USA',
            'HouseNumber': '1245',
            'StateProvince': 'Florida',
            'Street': 'Av. Collins',
            'ZipCode': '33140'
            }
    },
    'psp_ShippingDetails': {
        'TrackingNumber': '154DDD54DWW11',
        'Method': '1',
        'Carrier': '200',
        'DeliveryDate': '2014-11-20',
        'FreightAmount': '15000',
        'GiftMessage': 'Happy Birthday!',
        'GiftWrapping': '1',
        'PrimaryRecipient': {
            'DateOfBirth': '1979-01-12',
            'FirstName': 'John',
            'Gender': 'M',
            'IDNumber': '54111111',
            'IDType': '200',
            'LastName': 'Doe',
            'MiddleName': 'Michael',
            'Nationality': 'ARG',
            'PhoneNumber1': '+1 011 11111111',
            'PhoneNumber2': '+1 011 22222222'
            },
        'SecondaryRecipient': {
            'DateOfBirth': '1979-01-12',
            'FirstName': 'John',
            'Gender': 'M',
            'IDNumber': '54111111',
            'IDType': '200',
            'LastName': 'Doe',
            'MiddleName': 'Michael',
            'Nationality': 'ARG',
            'PhoneNumber1': '+1 011 11111111',
            'PhoneNumber2': '+1 011 22222222'
            },
        'Address': {
            'AdditionalInfo': '2 A',
            'City': 'Miami',
            'Country': 'USA',
            'HouseNumber': '1245',
            'StateProvince': 'Florida',
            'Street': 'Av. Collins',
            'ZipCode': '33140'
            }
    },
    'psp_OrderDetails': [
        {
            'Quantity': '10',
            'UnitPrice': '10050',
            'Description': 'Blue pencil',
            'Type': '1002',
            'SkuCode': 'SO-4587885545',
            'ManufacturerPartNumber': 'CN-0N2828421-3AD-02CD',
            'Risk': 'H'
        },
        {
            'Quantity': '10',
            'UnitPrice': '10050',
            'Description': 'Blue pencil',
            'Type': '1002',
            'SkuCode': 'SO-4587885545',
            'ManufacturerPartNumber': 'CN-0N2828421-3AD-02CD',
            'Risk': 'H'
        },
    ],
    'psp_AirlineDetails': {
        'PNR': '154DDD54DWW11',
        'Legs': [
            {
                'DepartureAirport': 'EZE',
                'DepartureDatetime': '2014-05-12 13:05:00',
                'DepartureAirportTimezone': '-03:00',
                'ArrivalAirport': 'AMS',
                'CarrierCode': 'KL',
                'FlightNumber': '842',
                'FareBasisCode': 'HL7LNR',
                'FareClassCode': 'FR',
                'BaseFare': '30000',
                'BaseFareCurrency': '032'
            }
        ],
        'Passengers': [
            {
                'FirstName': 'John',
                'LastName': 'Doe',
                'MiddleName': 'Michael',
                'Type': 'A',
                'DateOfBirth': '1979-01-12',
                'Nationality': 'ARG',
                'IDNumber': '54111111',
                'IDType': '100',
                'IDCountry': 'ARG',
                'LoyaltyNumber': '254587547',
                'LoyaltyTier': '1'
            }
        ],
        'Ticket': {
            'TicketNumber': '07411865255578',
            'Eticket': '1',
            'Restricted': '1',
            'Issue': {
                'CarrierCode': 'AA',
                'TravelAgentCode': '32165464',
                'TravelAgentName': 'Washington Hilton',
                'Date': '2017-01-10',
                'Country': 'ARG',
                'City': 'Buenos Aires',
                'Address': 'Av. Rivadavia 1111'
                    },
            'TotalFareAmount': '80000',
            'TotalTaxAmount': '25200',
            'TotalFeeAmount': '14800'
            }
    }
}