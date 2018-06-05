response = sdk.update_customer(params)

response[:psp_response_cod];
response[:psp_response_msg];
response[:psp_merchant_id];
response[:psp_customer_id];
response[:psp_email_address];
response[:psp_alternative_email_address];
response[:psp_account_id];
response[:psp_account_created_at];

pspPerson = response[:psp_person];
pspPerson[:first_name];
pspPerson[:last_name];
pspPerson[:middle_name];
pspPerson[:phone_number1];
pspPerson[:phone_number2];
pspPerson[:gender];
pspPerson[:date_of_birth];
pspPerson[:nationality];
pspPerson[:id_number];
pspPerson[:id_type];

pspAddress = response[:psp_address];
pspAddress[:street];
pspAddress[:house_number];
pspAddress[:additional_info];
pspAddress[:city];
pspAddress[:state_province];
pspAddress[:country];
pspAddress[:zip_code];
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
pspPaymentMethods0[:created_at];
pspPaymentMethods0[:updated_at];


response[:psp_pos_date_time];
