$ArraySplitPayOnline2pTransactions = array(
    'psp_MerchantId' => 'sdk_test',
    'psp_MerchTxRef' => 'ORDER1000-1',
    'psp_MerchAdditionalRef' => 'ADDITIONAL-REF1234',
    'psp_Product' => '14',
    'psp_CardNumber' => '4507990000000010',
    'psp_CardExpDate' => '1906',
    'psp_CardSecurityCode' => '321',
    'psp_CardHolderName' => 'JOHN DOE',
    'psp_PaymentAmount' => '10050',
    'psp_Amount' => '15050',
    'psp_NumPayments' => '1',
    'psp_SoftDescriptor' => 'Compra Art 15',
    'psp_AmountAdditionalDetails' => array(
        'Tip' => '20000',
        'Discount' => '11000',
        'Taxes' => array(
            array(
                'TypeId' => '500',
                'Amount' => '10000',
                'Rate' => '2100',
                'BaseAmount' => '10000'
            ),
            array(
                'TypeId' => '500',
                'Amount' => '10000',
                'Rate' => '2100',
                'BaseAmount' => '10000'
            ),
        )
    ),
    'psp_MerchantAdditionalDetails' => array(
        'Type' => '2 A',
        'SellerDetails' => array(
            'IDNumber' => '30706033471',
            'IDType' => '205',
            'Name' => 'Company S.A.',
            'Invoice' => '54877555',
            'PurchaseDescription' => 'Samsung 4K SUHD TV',
            'Address' => array(
                'AdditionalInfo' => '2 A',
                'City' => 'Miami',
                'Country' => 'USA',
                'HouseNumber' => '1245',
                'StateProvince' => 'Florida',
                'Street' => 'Av. Collins',
                'ZipCode' => '33140'
                    ),
            'MCC' => '5732',
            'ChannelCode' => '',
            'GeoCode' => ''
            )
    ),
    'psp_BillingDetails' => array(
        'Invoice' => '54877555',
        'InvoiceDate' => '2017-10-23',
        'InvoiceAmount' => '15050',
        'InvoiceCurrency' => '032',
        'Person' => array(
            'DateOfBirth' => '1979-01-12',
            'FirstName' => 'John',
            'Gender' => 'M',
            'IDNumber' => '54111111',
            'IDType' => '200',
            'LastName' => 'Doe',
            'MiddleName' => 'Michael',
            'Nationality' => 'ARG',
            'PhoneNumber1' => '+1 011 11111111',
            'PhoneNumber2' => '+1 011 22222222'
            ),
        'Address' => array(
            'AdditionalInfo' => '2 A',
            'City' => 'Miami',
            'Country' => 'USA',
            'HouseNumber' => '1245',
            'StateProvince' => 'Florida',
            'Street' => 'Av. Collins',
            'ZipCode' => '33140'
            )
    ),
    'psp_VaultReference' => array(
        'PaymentMethodId' => 'Nzmd7DyGytXXC5PtKwnCsXXuQWHJB9EE',
        'CustomerId' => 'K8sj5rBrGqPBczTR4LtuKE6g4iZMmY9f'
    )
);