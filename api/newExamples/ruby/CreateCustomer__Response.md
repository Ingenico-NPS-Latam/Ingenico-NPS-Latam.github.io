response = sdk.create_customer(params)

response[:psp_response_cod];
response[:psp_response_msg];
response[:psp_merchant_id];
response[:psp_customer_id];
response[:psp_email_address];
response[:psp_alternative_email_address];
response[:psp_account_id];
response[:psp_account_created_at];
response[:psp_default_payment_method_id];

pspPaymentMethods0 = response[:psp_payment_methods][0];

pspPaymentMethods0[:payment_method_id];
pspPaymentMethods0[:product];

cardOutputDetails = pspPaymentMethods0[:card_output_details];
cardOutputDetails[:expiration_date];
cardOutputDetails[:expiration_year];
cardOutputDetails[:expiration_month];
cardOutputDetails[:holder_name];
cardOutputDetails[:iin];
cardOutputDetails[:last4];
cardOutputDetails[:number_length];
cardOutputDetails[:masked_number];
cardOutputDetails[:masked_number_alternative];
pspPaymentMethods0[:finger_print];

person = pspPaymentMethods0[:person];
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

address = pspPaymentMethods0[:address];
address[:street];
address[:house_number];
address[:additional_info];
address[:city];
address[:state_province];
address[:country];
address[:zip_code];
pspPaymentMethods0[:created_at];
pspPaymentMethods0[:updated_at];


response[:psp_pos_date_time];
