var response = NPS.card.getInstallmentsOptions(psp_PaymentMethodToken, psp_Product, psp_NumPayments);

console.log(response)
console.log(response.length)

console.log(response[Object.keys(response)[0]])
console.log(response[Object.keys(response)[0]].num_payments)
console.log(response[Object.keys(response)[0]].installment_amount)