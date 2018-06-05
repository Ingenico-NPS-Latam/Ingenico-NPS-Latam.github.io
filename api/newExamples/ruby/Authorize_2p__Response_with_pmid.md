response = sdk.authorize_2p(params)

response[:psp_response_cod];
response[:psp_response_msg];
response[:psp_response_extended];
response[:psp_transaction_id];
response[:psp_merchant_id];
response[:psp_merch_tx_ref];
response[:psp_merch_order_id];
response[:psp_amount];
response[:psp_num_payments];
response[:psp_currency];
response[:psp_country];
response[:psp_product];
response[:psp_card_exp_date];
response[:psp_authorization_code];
response[:psp_batch_nro];
response[:psp_ticket_number];
response[:psp_cl_external_merchant];
response[:psp_cl_external_terminal];
response[:psp_cl_response_cod];
response[:psp_cl_response_msg];
response[:psp_pos_date_time];
response[:psp_created_at];

pspFraudScreeningResult = response[:psp_fraud_screening_result];
pspFraudScreeningResult[:result_code];
pspFraudScreeningResult[:result_description];

pspVerificationServicesResult = response[:psp_verification_services_result];
pspVerificationServicesResult[:result_code_card_security_code];
pspVerificationServicesResult[:result_code_billing_address];
pspVerificationServicesResult[:result_code_billing_address_zip_code];
pspVerificationServicesResult[:result_code_billing_person_id_type];
pspVerificationServicesResult[:result_code_billing_person_id_number];
pspVerificationServicesResult[:result_code_billing_person_date_of_birth];
pspVerificationServicesResult[:result_code_billing_person_name];
pspVerificationServicesResult[:result_code_billing_person_phone_number1];
pspVerificationServicesResult[:result_code_customer_email_address];
