response = sdk.create_payment_method_token(params)

response[:psp_response_cod];
response[:psp_response_msg];
response[:psp_merchant_id];
response[:psp_payment_method_token];
response[:psp_product];

pspCardOutputDetails = response[:psp_card_output_details];
pspCardOutputDetails[:expiration_date];
pspCardOutputDetails[:expiration_year];
pspCardOutputDetails[:expiration_month];
pspCardOutputDetails[:holder_name];
pspCardOutputDetails[:iin];
pspCardOutputDetails[:last4];
pspCardOutputDetails[:number_length];
pspCardOutputDetails[:masked_number];
pspCardOutputDetails[:masked_number_alternative];
response[:psp_already_used];
response[:psp_created_at];
response[:psp_updated_at];
