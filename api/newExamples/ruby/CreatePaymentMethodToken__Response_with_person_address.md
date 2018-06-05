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
response[:psp_already_used];
response[:psp_created_at];
response[:psp_updated_at];
