response = sdk.fraud_screening(params)

response[:psp_response_cod];
response[:psp_response_msg];

pspResult = response[:psp_result];
pspResult[:result_code];
pspResult[:result_description];
response[:psp_order_id];
response[:psp_merchant_id];
response[:psp_merch_tx_ref];
response[:psp_merch_order_id];
response[:psp_amount];
response[:psp_num_payments];
response[:psp_currency];
response[:psp_country];
response[:psp_product];
response[:psp_card_exp_date];
response[:psp_pos_date_time];
