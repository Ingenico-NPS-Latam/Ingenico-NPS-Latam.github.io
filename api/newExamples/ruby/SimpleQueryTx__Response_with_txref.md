response = sdk.simple_query_tx(params)

response[:psp_response_cod];
response[:psp_response_msg];
response[:psp_merchant_id];
response[:psp_query_criteria];
response[:psp_query_criteria_id];
response[:psp_pos_date_time];

pspTransaction = response[:psp_transaction];
pspTransaction[:psp_response_cod];
pspTransaction[:psp_response_msg];
pspTransaction[:psp_response_extended];
pspTransaction[:psp_transaction_id];
pspTransaction[:psp_merchant_id];
pspTransaction[:psp_tx_source];
pspTransaction[:psp_operation];
pspTransaction[:psp_merch_tx_ref];
pspTransaction[:psp_merch_order_id];
pspTransaction[:psp_amount];
pspTransaction[:psp_num_payments];
pspTransaction[:psp_currency];
pspTransaction[:psp_country];
pspTransaction[:psp_product];
pspTransaction[:psp_authorization_code];
pspTransaction[:psp_batch_nro];
pspTransaction[:psp_ticket_number];
pspTransaction[:psp_card_number_fsd];
pspTransaction[:psp_card_number_lfd];
pspTransaction[:psp_card_mask];
pspTransaction[:psp_cl_external_merchant];
pspTransaction[:psp_cl_external_terminal];
pspTransaction[:psp_cl_response_cod];
pspTransaction[:psp_cl_response_msg];
pspTransaction[:psp_pos_date_time];
pspTransaction[:psp_created_at];

pspFraudScreeningResult = pspTransaction[:psp_fraud_screening_result];
pspFraudScreeningResult[:result_code];
pspFraudScreeningResult[:result_description];

pspVerificationServicesResult = pspTransaction[:psp_verification_services_result];
pspVerificationServicesResult[:result_code_card_security_code];
pspVerificationServicesResult[:result_code_billing_address];
pspVerificationServicesResult[:result_code_billing_address_zip_code];
pspVerificationServicesResult[:result_code_billing_person_id_type];
pspVerificationServicesResult[:result_code_billing_person_id_number];
pspVerificationServicesResult[:result_code_billing_person_date_of_birth];
pspVerificationServicesResult[:result_code_billing_person_name];
pspVerificationServicesResult[:result_code_billing_person_phone_number1];
pspVerificationServicesResult[:result_code_customer_email_address];
