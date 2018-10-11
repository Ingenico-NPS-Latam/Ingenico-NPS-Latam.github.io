response = sdk.retrieve_payment_method_token(params)

response[:psp_response_cod];
response[:psp_response_msg];
response[:psp_merchant_id];
response[:psp_payment_method_token];
response[:psp_product];

pspWalletOutputDetails = response[:psp_wallet_output_details];

cardOutputDetails = pspWalletOutputDetails[:card_output_details];
cardOutputDetails[:expiration_date];
cardOutputDetails[:expiration_year];
cardOutputDetails[:expiration_month];
cardOutputDetails[:holder_name];
cardOutputDetails[:iin];
cardOutputDetails[:last4];
cardOutputDetails[:number_length];
cardOutputDetails[:masked_number];
cardOutputDetails[:masked_number_alternative];

shippingDetails = pspWalletOutputDetails[:shipping_details];
shippingDetails[:method];

primaryRecipient = shippingDetails[:primary_recipient];
primaryRecipient[:first_name];
primaryRecipient[:phone_number1];

address = shippingDetails[:address];
address[:street];

houseNumber = address[:house_number];
address[:additional_info];
address[:city];
address[:country];
address[:zip_code];

pspAddress = response[:psp_address];
pspAddress[:street];
pspAddress[:additional_info];
pspAddress[:city];
pspAddress[:country];
pspAddress[:zip_code];
response[:psp_already_used];
response[:psp_created_at];
response[:psp_updated_at];
