RootElement data = new RootElement();

data.Add("psp_TransactionId", "100022");
data.Add("psp_MerchantId", "sdk_test");
data.Add("psp_MerchTxRef", "ORDER1000-1");
data.Add("psp_MerchOrderId", "ORDER1000");
data.Add("psp_MerchAdditionalRef", "ADDITIONAL-REF1234");
data.Add("psp_Amount", "15050");
data.Add("psp_NumPayments", "1");
data.Add("psp_PaymentAmount", "10050");
data.Add("psp_Product", "14");
data.Add("psp_CardNumber", "4507990000000010");
data.Add("psp_CardExpDate", "1906");
data.Add("psp_AuthorizationCode", "352123");
data.Add("psp_BatchNro", "1254");
data.Add("psp_SequenceNumber", "64564321654");
data.Add("psp_TicketNumber", "1254");
data.Add("psp_ClTrnId", "365258");
data.Add("psp_ClExternalMerchant", "96878987");
data.Add("psp_ClExternalTerminal", "14587986");
data.Add("psp_ClResponseCod", "155");
data.Add("psp_ClResponseMsg", "33140");
data.Add("psp_Plan", "PlanZ");
data.Add("psp_CreatedAt", "2008-01-12 13:05:35-03:00");

ComplexElement pspAmountAdditionalDetails = new ComplexElement();
pspAmountAdditionalDetails.Add("Tip", "20000");
pspAmountAdditionalDetails.Add("Discount", "11000");

ComplexElementArray Taxes = new ComplexElementArray();

ComplexElementArrayItem Taxes1 = new ComplexElementArrayItem();
Taxes1.Add("TypeId", "500");
Taxes1.Add("Amount", "10000");
Taxes1.Add("Rate", "2100");
Taxes1.Add("BaseAmount", "10000");

Taxes.Add(Taxes1);

ComplexElementArrayItem Taxes2 = new ComplexElementArrayItem();
Taxes2.Add("TypeId", "500");
Taxes2.Add("Amount", "10000");
Taxes2.Add("Rate", "2100");
Taxes2.Add("BaseAmount", "10000");

Taxes.Add(Taxes2);

pspAmountAdditionalDetails.Add("Taxes", Taxes);

data.Add("psp_AmountAdditionalDetails", pspAmountAdditionalDetails);

ComplexElement pspFraudScreeningResult = new ComplexElement();
pspFraudScreeningResult.Add("ResultCode", "A");
pspFraudScreeningResult.Add("ResultDescription", "ACCEPT");
pspFraudScreeningResult.Add("AdditionalInfo", "Information");

data.Add("psp_FraudScreeningResult", pspFraudScreeningResult);

ComplexElement pspVerificationServicesResult = new ComplexElement();
pspVerificationServicesResult.Add("ResultCodeCardSecurityCode", "M");
pspVerificationServicesResult.Add("ResultCodeBillingAddress", "M");
pspVerificationServicesResult.Add("ResultCodeBillingAddressZipCode", "M");
pspVerificationServicesResult.Add("ResultCodeBillingPersonIDType", "M");
pspVerificationServicesResult.Add("ResultCodeBillingPersonIDNumber", "M");
pspVerificationServicesResult.Add("ResultCodeBillingPersonDateOfBirth", "M");
pspVerificationServicesResult.Add("ResultCodeBillingPersonName", "M");
pspVerificationServicesResult.Add("ResultCodeBillingPersonPhoneNumber1", "M");
pspVerificationServicesResult.Add("ResultCodeCustomerEmailAddress", "M");

data.Add("psp_VerificationServicesResult", pspVerificationServicesResult);
