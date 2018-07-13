RootElement data = new RootElement();

data.add("psp_TransactionId", "100022");
data.add("psp_MerchantId", "sdk_test");
data.add("psp_MerchTxRef", "ORDER1000-1");
data.add("psp_MerchOrderId", "ORDER1000");
data.add("psp_MerchAdditionalRef", "ADDITIONAL-REF1234");
data.add("psp_Amount", "15050");
data.add("psp_NumPayments", "1");
data.add("psp_PaymentAmount", "10050");
data.add("psp_Product", "14");
data.add("psp_CardNumber", "4507990000000010");
data.add("psp_CardExpDate", "1906");
data.add("psp_AuthorizationCode", "352123");
data.add("psp_BatchNro", "1254");
data.add("psp_SequenceNumber", "64564321654");
data.add("psp_TicketNumber", "1254");
data.add("psp_ClTrnId", "365258");
data.add("psp_ClExternalMerchant", "96878987");
data.add("psp_ClExternalTerminal", "14587986");
data.add("psp_ClResponseCod", "155");
data.add("psp_ClResponseMsg", "33140");
data.add("psp_Plan", "PlanZ");
data.add("psp_CreatedAt", "2008-01-12 13:05:35-03:00");

ComplexElement pspAmountAdditionalDetails = new ComplexElement();
pspAmountAdditionalDetails.add("Tip", "20000");
pspAmountAdditionalDetails.add("Discount", "11000");

ComplexElementArray Taxes = new ComplexElementArray();

ComplexElementArrayItem Taxes1 = new ComplexElementArrayItem();
Taxes1.add("TypeId", "500");
Taxes1.add("Amount", "10000");
Taxes1.add("Rate", "2100");
Taxes1.add("BaseAmount", "10000");

Taxes.add(Taxes1);

ComplexElementArrayItem Taxes2 = new ComplexElementArrayItem();
Taxes2.add("TypeId", "500");
Taxes2.add("Amount", "10000");
Taxes2.add("Rate", "2100");
Taxes2.add("BaseAmount", "10000");

Taxes.add(Taxes2);

pspAmountAdditionalDetails.add("Taxes", Taxes);

data.add("psp_AmountAdditionalDetails", pspAmountAdditionalDetails);

ComplexElement pspFraudScreeningResult = new ComplexElement();
pspFraudScreeningResult.add("ResultCode", "A");
pspFraudScreeningResult.add("ResultDescription", "ACCEPT");
pspFraudScreeningResult.add("AdditionalInfo", "Information");

data.add("psp_FraudScreeningResult", pspFraudScreeningResult);

ComplexElement pspVerificationServicesResult = new ComplexElement();
pspVerificationServicesResult.add("ResultCodeCardSecurityCode", "M");
pspVerificationServicesResult.add("ResultCodeBillingAddress", "M");
pspVerificationServicesResult.add("ResultCodeBillingAddressZipCode", "M");
pspVerificationServicesResult.add("ResultCodeBillingPersonIDType", "M");
pspVerificationServicesResult.add("ResultCodeBillingPersonIDNumber", "M");
pspVerificationServicesResult.add("ResultCodeBillingPersonDateOfBirth", "M");
pspVerificationServicesResult.add("ResultCodeBillingPersonName", "M");
pspVerificationServicesResult.add("ResultCodeBillingPersonPhoneNumber1", "M");
pspVerificationServicesResult.add("ResultCodeCustomerEmailAddress", "M");

data.add("psp_VerificationServicesResult", pspVerificationServicesResult);
