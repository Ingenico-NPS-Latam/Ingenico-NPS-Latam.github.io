response = sdk.create_payment_method_from_payment(params)

response[:psp_response_cod];
response[:psp_response_msg];
response[:psp_merchant_id];

pspPaymentMethod = response[:psp_payment_method];
pspPaymentMethod[:payment_method_id];
pspPaymentMethod[:payment_method_tag];
pspPaymentMethod[:product];

cardOutputDetails = pspPaymentMethod[:card_output_details];
cardOutputDetails[:expiration_date];
cardOutputDetails[:expiration_year];
cardOutputDetails[:expiration_month];
cardOutputDetails[:iin];
cardOutputDetails[:last4];
cardOutputDetails[:number_length];
cardOutputDetails[:masked_number];
cardOutputDetails[:masked_number_alternative];
pspPaymentMethod[:finger_print];
pspPaymentMethod[:created_at];
pspPaymentMethod[:updated_at];
response[:psp_pos_date_time];
