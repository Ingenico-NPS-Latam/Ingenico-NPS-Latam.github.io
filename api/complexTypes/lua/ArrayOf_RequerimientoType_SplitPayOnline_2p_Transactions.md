ArraySplitPayOnline2pTransactions = {}

ArraySplitPayOnline2pTransactions.psp_MerchantId = "sdk_test"
ArraySplitPayOnline2pTransactions.psp_MerchTxRef = "ORDER1000-1"
ArraySplitPayOnline2pTransactions.psp_MerchAdditionalRef = "ADDITIONAL-REF1234"
ArraySplitPayOnline2pTransactions.psp_Product = "14"
ArraySplitPayOnline2pTransactions.psp_CardNumber = "4507990000000010"
ArraySplitPayOnline2pTransactions.psp_CardExpDate = "1906"
ArraySplitPayOnline2pTransactions.psp_CardSecurityCode = "321"
ArraySplitPayOnline2pTransactions.psp_CardHolderName = "JOHN DOE"
ArraySplitPayOnline2pTransactions.psp_PaymentAmount = "10050"
ArraySplitPayOnline2pTransactions.psp_Amount = "15050"
ArraySplitPayOnline2pTransactions.psp_NumPayments = "1"
ArraySplitPayOnline2pTransactions.psp_SoftDescriptor = "Compra Art 15"

pspAmountAdditionalDetails = {}
pspAmountAdditionalDetails.Tip = "20000"
pspAmountAdditionalDetails.Discount = "11000"

Taxes = {}

Taxes1 = {}
Taxes1.TypeId = "500"
Taxes1.Amount = "10000"
Taxes1.Rate = "2100"
Taxes1.BaseAmount = "10000"

Taxes[#Taxes+1] = Taxes1

Taxes2 = {}
Taxes2.TypeId = "500"
Taxes2.Amount = "10000"
Taxes2.Rate = "2100"
Taxes2.BaseAmount = "10000"

Taxes[#Taxes+1] = Taxes2

pspAmountAdditionalDetails.Taxes = Taxes

ArraySplitPayOnline2pTransactions.psp_AmountAdditionalDetails = pspAmountAdditionalDetails

pspMerchantAdditionalDetails = {}
pspMerchantAdditionalDetails.Type = "2 A"

SellerDetails = {}
SellerDetails.IDNumber = "30706033471"
SellerDetails.IDType = "205"
SellerDetails.Name = "Company S.A."
SellerDetails.Invoice = "54877555"
SellerDetails.PurchaseDescription = "Samsung 4K SUHD TV"

Address = {}
Address.AdditionalInfo = "2 A"
Address.City = "Miami"
Address.Country = "USA"
Address.HouseNumber = "1245"
Address.StateProvince = "Florida"
Address.Street = "Av. Collins"
Address.ZipCode = "33140"

SellerDetails.Address = Address
SellerDetails.MCC = "5732"
SellerDetails.ChannelCode = ""
SellerDetails.GeoCode = ""

pspMerchantAdditionalDetails.SellerDetails = SellerDetails

ArraySplitPayOnline2pTransactions.psp_MerchantAdditionalDetails = pspMerchantAdditionalDetails

pspBillingDetails = {}
pspBillingDetails.Invoice = "54877555"
pspBillingDetails.InvoiceDate = "2017-10-23"
pspBillingDetails.InvoiceAmount = "15050"
pspBillingDetails.InvoiceCurrency = "032"

Person = {}
Person.DateOfBirth = "1979-01-12"
Person.FirstName = "John"
Person.Gender = "M"
Person.IDNumber = "54111111"
Person.IDType = "200"
Person.LastName = "Doe"
Person.MiddleName = "Michael"
Person.Nationality = "ARG"
Person.PhoneNumber1 = "+1 011 11111111"
Person.PhoneNumber2 = "+1 011 22222222"

pspBillingDetails.Person = Person

Address = {}
Address.AdditionalInfo = "2 A"
Address.City = "Miami"
Address.Country = "USA"
Address.HouseNumber = "1245"
Address.StateProvince = "Florida"
Address.Street = "Av. Collins"
Address.ZipCode = "33140"

pspBillingDetails.Address = Address

ArraySplitPayOnline2pTransactions.psp_BillingDetails = pspBillingDetails

pspVaultReference = {}
pspVaultReference.PaymentMethodId = "Nzmd7DyGytXXC5PtKwnCsXXuQWHJB9EE"
pspVaultReference.CustomerId = "K8sj5rBrGqPBczTR4LtuKE6g4iZMmY9f"

ArraySplitPayOnline2pTransactions.psp_VaultReference = pspVaultReference
