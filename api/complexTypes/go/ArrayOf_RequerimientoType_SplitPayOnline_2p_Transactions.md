ArraySplitPayOnline2pTransactions := nps.NewArraySplitPayOnline2pTransactionsStruct()
ArraySplitPayOnline2pTransactions.Psp_MerchantId = "sdk_test"
ArraySplitPayOnline2pTransactions.Psp_MerchTxRef = "ORDER1000-1"
ArraySplitPayOnline2pTransactions.Psp_MerchAdditionalRef = "ADDITIONAL-REF1234"
ArraySplitPayOnline2pTransactions.Psp_Product = "14"
ArraySplitPayOnline2pTransactions.Psp_CardNumber = "4507990000000010"
ArraySplitPayOnline2pTransactions.Psp_CardExpDate = "1906"
ArraySplitPayOnline2pTransactions.Psp_CardSecurityCode = "321"
ArraySplitPayOnline2pTransactions.Psp_CardHolderName = "JOHN DOE"
ArraySplitPayOnline2pTransactions.Psp_PaymentAmount = "10050"
ArraySplitPayOnline2pTransactions.Psp_Amount = "15050"
ArraySplitPayOnline2pTransactions.Psp_NumPayments = "1"
ArraySplitPayOnline2pTransactions.Psp_SoftDescriptor = "Compra Art 15"

pspAmountAdditionalDetails := nps.NewAmountAdditionalDetailsRequestStruct()
pspAmountAdditionalDetails.Tip = "20000"
pspAmountAdditionalDetails.Discount = "11000"

Taxes := nps.NewArrayOf_TaxesRequestStruct()
Taxes.Items = make([]*nps.NewTaxesRequestStruct(), 0)

Taxes1 := nps.NewTaxesRequestStruct()
Taxes1.TypeId = "500"
Taxes1.Amount = "10000"
Taxes1.Rate = "2100"
Taxes1.BaseAmount = "10000"
Taxes.Items = append(Taxes.Items, Taxes1)

Taxes2 := nps.NewTaxesRequestStruct()
Taxes2.TypeId = "500"
Taxes2.Amount = "10000"
Taxes2.Rate = "2100"
Taxes2.BaseAmount = "10000"
Taxes.Items = append(Taxes.Items, Taxes2)


ArraySplitPayOnline2pTransactions.psp_AmountAdditionalDetails = pspAmountAdditionalDetails

pspMerchantAdditionalDetails := nps.NewMerchantAdditionalDetailsStruct()
pspMerchantAdditionalDetails.Type = "2 A"

SellerDetails := nps.NewSellerDetailsStruct()
SellerDetails.IDNumber = "30706033471"
SellerDetails.IDType = "205"
SellerDetails.Name = "Company S.A."
SellerDetails.Invoice = "54877555"
SellerDetails.PurchaseDescription = "Samsung 4K SUHD TV"

Address := nps.NewAddressStruct()
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

pspBillingDetails := nps.NewBillingDetailsStruct()
pspBillingDetails.Invoice = "54877555"
pspBillingDetails.InvoiceDate = "2017-10-23"
pspBillingDetails.InvoiceAmount = "15050"
pspBillingDetails.InvoiceCurrency = "032"

Person := nps.NewPersonStruct()
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

Address := nps.NewAddressStruct()
Address.AdditionalInfo = "2 A"
Address.City = "Miami"
Address.Country = "USA"
Address.HouseNumber = "1245"
Address.StateProvince = "Florida"
Address.Street = "Av. Collins"
Address.ZipCode = "33140"

pspBillingDetails.Address = Address

ArraySplitPayOnline2pTransactions.psp_BillingDetails = pspBillingDetails

pspVaultReference := nps.NewVaultReferenceStruct()
pspVaultReference.PaymentMethodId = "Nzmd7DyGytXXC5PtKwnCsXXuQWHJB9EE"
pspVaultReference.CustomerId = "K8sj5rBrGqPBczTR4LtuKE6g4iZMmY9f"

ArraySplitPayOnline2pTransactions.psp_VaultReference = pspVaultReference
