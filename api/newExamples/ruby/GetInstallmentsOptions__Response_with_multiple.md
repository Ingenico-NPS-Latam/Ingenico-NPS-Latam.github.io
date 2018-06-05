response = sdk.get_installments_options(params)

response[:psp_response_cod];
response[:psp_response_msg];
response[:psp_merchant_id];
response[:psp_amount];
response[:psp_product];
response[:psp_currency];
response[:psp_country];
response[:psp_num_payments];

pspInstallmentsOptions0 = response[:psp_installments_options][0];

pspInstallmentsOptions0[:num_payments];
pspInstallmentsOptions0[:installment_amount];


response[:psp_pos_date_time];
