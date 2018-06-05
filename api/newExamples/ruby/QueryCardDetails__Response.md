response = sdk.query_card_details(params)

response[:psp_response_cod];
response[:psp_response_msg];
response[:psp_merchant_id];
response[:psp_query_criteria];
response[:psp_query_criteria_id];
response[:psp_pos_date_time];

pspCardOutputDetails = response[:psp_card_output_details];
pspCardOutputDetails[:number];
pspCardOutputDetails[:expiration_date];
pspCardOutputDetails[:expiration_year];
pspCardOutputDetails[:expiration_month];
pspCardOutputDetails[:holder_name];
pspCardOutputDetails[:ii_n];
pspCardOutputDetails[:last4];
pspCardOutputDetails[:number_length];
pspCardOutputDetails[:masked_number];
pspCardOutputDetails[:masked_number_alternative];

