response = sdk.query_txs(params)

response[:psp_response_cod];
response[:psp_response_msg];
response[:psp_merchant_id];
response[:psp_query_criteria];
response[:psp_query_criteria_id];
response[:psp_pos_date_time];

pspTransactions0 = response[:psp_transactions][0];

pspTransactions0[:psp_response_cod];
pspTransactions0[:psp_response_msg];
pspTransactions0[:psp_response_extended];
pspTransactions0[:psp_transaction_id];
pspTransactions0[:psp_merchant_id];
pspTransactions0[:psp_tx_source];
pspTransactions0[:psp_operation];
pspTransactions0[:psp_merch_tx_ref];
pspTransactions0[:psp_merch_order_id];
pspTransactions0[:psp_amount];
pspTransactions0[:psp_num_payments];
pspTransactions0[:psp_currency];
pspTransactions0[:psp_country];
pspTransactions0[:psp_product];
pspTransactions0[:psp_authorization_code];
pspTransactions0[:psp_batch_nro];
pspTransactions0[:psp_ticket_number];
pspTransactions0[:psp_card_number_fsd];
pspTransactions0[:psp_card_number_lfd];
pspTransactions0[:psp_card_mask];
pspTransactions0[:psp_cl_external_merchant];
pspTransactions0[:psp_cl_external_terminal];
pspTransactions0[:psp_cl_response_cod];
pspTransactions0[:psp_cl_response_msg];
pspTransactions0[:psp_pos_date_time];
pspTransactions0[:psp_created_at];

pspFraudScreeningResult = pspTransactions0[:psp_fraud_screening_result];
pspFraudScreeningResult[:result_code];
pspFraudScreeningResult[:result_description];

pspVerificationServicesResult = pspTransactions0[:psp_verification_services_result];
pspVerificationServicesResult[:result_code_card_security_code];
pspVerificationServicesResult[:result_code_billing_address];
pspVerificationServicesResult[:result_code_billing_address_zip_code];
pspVerificationServicesResult[:result_code_billing_person_id_type];
pspVerificationServicesResult[:result_code_billing_person_id_number];
pspVerificationServicesResult[:result_code_billing_person_date_of_birth];
pspVerificationServicesResult[:result_code_billing_person_name];
pspVerificationServicesResult[:result_code_billing_person_phone_number1];
pspVerificationServicesResult[:result_code_customer_email_address];

pspTransactions1 = response[:psp_transactions][1];

pspTransactions1[:psp_response_cod];
pspTransactions1[:psp_response_msg];
pspTransactions1[:psp_response_extended];
pspTransactions1[:psp_transaction_id];
pspTransactions1[:psp_merchant_id];
pspTransactions1[:psp_tx_source];
pspTransactions1[:psp_operation];
pspTransactions1[:psp_merch_tx_ref];
pspTransactions1[:psp_merch_order_id];
pspTransactions1[:psp_amount];
pspTransactions1[:psp_num_payments];
pspTransactions1[:psp_currency];
pspTransactions1[:psp_country];
pspTransactions1[:psp_product];
pspTransactions1[:psp_authorization_code];
pspTransactions1[:psp_batch_nro];
pspTransactions1[:psp_ticket_number];
pspTransactions1[:psp_card_number_fsd];
pspTransactions1[:psp_card_number_lfd];
pspTransactions1[:psp_card_mask];
pspTransactions1[:psp_cl_external_merchant];
pspTransactions1[:psp_cl_external_terminal];
pspTransactions1[:psp_cl_response_cod];
pspTransactions1[:psp_cl_response_msg];
pspTransactions1[:psp_pos_date_time];
pspTransactions1[:psp_created_at];

pspFraudScreeningResult = pspTransactions1[:psp_fraud_screening_result];
pspFraudScreeningResult[:result_code];
pspFraudScreeningResult[:result_description];

pspVerificationServicesResult = pspTransactions1[:psp_verification_services_result];
pspVerificationServicesResult[:result_code_card_security_code];
pspVerificationServicesResult[:result_code_billing_address];
pspVerificationServicesResult[:result_code_billing_address_zip_code];
pspVerificationServicesResult[:result_code_billing_person_id_type];
pspVerificationServicesResult[:result_code_billing_person_id_number];
pspVerificationServicesResult[:result_code_billing_person_date_of_birth];
pspVerificationServicesResult[:result_code_billing_person_name];
pspVerificationServicesResult[:result_code_billing_person_phone_number1];
pspVerificationServicesResult[:result_code_customer_email_address];


