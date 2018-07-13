ArraySplitAuthorize3pTransactions = {
    'psp_MerchantId' => 'sdk_test',
    'psp_MerchTxRef' => 'ORDER1000-1',
    'psp_MerchAdditionalRef' => 'ADDITIONAL-REF1234',
    'psp_Product' => '14',
    'psp_PromotionCore' => 'VISA SANTANDER',
    'psp_Amount' => '15050',
    'psp_NumPayments' => '1',
    'psp_SoftDescriptor' => 'Compra Art 15',
    'psp_AmountAdditionalDetails'  => {
        'Tip' => '20000',
        'Discount' => '11000',
        'Taxes'  => [
            {
                'TypeId' => '500',
                'Amount' => '10000',
                'Rate' => '2100',
                'BaseAmount' => '10000'
            },
            {
                'TypeId' => '500',
                'Amount' => '10000',
                'Rate' => '2100',
                'BaseAmount' => '10000'
            },
        ]
    }
}