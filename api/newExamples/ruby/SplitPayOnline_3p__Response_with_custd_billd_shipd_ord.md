response = sdk.split_pay_online_3p(params)

response[:psp_response_cod];
response[:psp_response_msg];
response[:psp_transaction_id];
response[:psp_session3p];
response[:psp_front_psp_url];
response[:psp_merchant_id];
response[:psp_merch_tx_ref];
response[:psp_merch_order_id];
response[:psp_amount];
response[:psp_currency];
response[:psp_country];
response[:psp_product];
response[:psp_customer_mail];
response[:psp_pos_date_time];

pspTransactions0 = response[:psp_transactions][0];

pspTransactions0[:psp_merchant_id];
pspTransactions0[:psp_transaction_id];
pspTransactions0[:psp_merch_tx_ref];
pspTransactions0[:psp_product];
pspTransactions0[:psp_amount];
pspTransactions0[:psp_num_payments];
pspTransactions0[:psp_created_at];

pspTransactions1 = response[:psp_transactions][1];

pspTransactions1[:psp_merchant_id];
pspTransactions1[:psp_transaction_id];
pspTransactions1[:psp_merch_tx_ref];
pspTransactions1[:psp_product];
pspTransactions1[:psp_amount];
pspTransactions1[:psp_num_payments];
pspTransactions1[:psp_created_at];


