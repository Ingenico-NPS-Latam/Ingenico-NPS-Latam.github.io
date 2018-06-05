response = sdk.delete_payment_method(params)

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
cardOutputDetails[:holder_name];
cardOutputDetails[:iin];
cardOutputDetails[:last4];
cardOutputDetails[:number_length];
cardOutputDetails[:masked_number];
cardOutputDetails[:masked_number_alternative];
pspPaymentMethod[:finger_print];

person = pspPaymentMethod[:person];
person[:first_name];
person[:last_name];
person[:middle_name];
person[:phone_number1];
person[:phone_number2];
person[:gender];
person[:date_of_birth];
person[:nationality];
person[:id_number];
person[:id_type];

address = pspPaymentMethod[:address];
address[:street];
address[:house_number];
address[:additional_info];
address[:city];
address[:state_province];
address[:country];
address[:zip_code];
pspPaymentMethod[:created_at];
pspPaymentMethod[:updated_at];
response[:psp_pos_date_time];
