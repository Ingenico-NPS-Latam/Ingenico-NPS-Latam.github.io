package main

import (
    "fmt"
    "github.com/Ingenico-NPS-Latam/nps-sdk-go/npsSdk"
    CONSTANTS "github.com/Ingenico-NPS-Latam/nps-sdk-go/npsSdk/constants"
)

func main() {

err := npsSdk.Configure(map[string]interface{}(
    "environment": CONSTANTS.SANDBOX_ENV,
    "secret_key": "_YOUR_SECRET_KEY_",
    "debug": true,
    "log_level": CONSTANTS.DEBUG,
})

service := npsSdk.NewPaymentServicePlatformPortType(true)

SplitPayOnLine3p := npsSdk.NewRequerimientoStruct_SplitPayOnLine_3p()

SplitPayOnLine3p.Psp_Version = "2.2"
SplitPayOnLine3p.Psp_MerchantId = "sdk_test"
SplitPayOnLine3p.Psp_TxSource = "WEB"
SplitPayOnLine3p.Psp_MerchOrderId = "ORDER66666"
SplitPayOnLine3p.Psp_ReturnURL = "http://localhost/"
SplitPayOnLine3p.Psp_FrmLanguage = "es_AR"
SplitPayOnLine3p.Psp_Amount = "15050"
SplitPayOnLine3p.Psp_Currency = "032"
SplitPayOnLine3p.Psp_Country = "ARG"
SplitPayOnLine3p.Psp_Product = "14"
SplitPayOnLine3p.Psp_PosDateTime = "2019-12-01 12:00:00"

pspCustomerAdditionalDetails := nps.NewCustomerAdditionalDetailsStruct()
pspCustomerAdditionalDetails.EmailAddress = "jdoe@email.com"
pspCustomerAdditionalDetails.AlternativeEmailAddress = "Jdoe79@email.com"
pspCustomerAdditionalDetails.IPAddress = "192.168.158.190"
pspCustomerAdditionalDetails.AccountID = "Jdoe78"
pspCustomerAdditionalDetails.AccountCreatedAt = "2010-10-23"
pspCustomerAdditionalDetails.AccountPreviousActivity = "1"
pspCustomerAdditionalDetails.AccountHasCredentials = "1"
pspCustomerAdditionalDetails.DeviceType = "1"
pspCustomerAdditionalDetails.DeviceFingerPrint = "KJhKHKJgh7777kgh..."
pspCustomerAdditionalDetails.BrowserLanguage = "ES"
pspCustomerAdditionalDetails.HttpUserAgent = "Mozilla/5.0 (X11; Ubuntu; Linux x86_64; rv:21.0) Gecko/20100101 Firefox/21.0"

SplitPayOnLine3p.psp_CustomerAdditionalDetails = pspCustomerAdditionalDetails

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

SplitPayOnLine3p.psp_BillingDetails = pspBillingDetails

pspShippingDetails := nps.NewShippingDetailsStruct()
pspShippingDetails.TrackingNumber = "154DDD54DWW11"
pspShippingDetails.Method = "10"
pspShippingDetails.Carrier = "200"
pspShippingDetails.DeliveryDate = "2014-11-20"
pspShippingDetails.FreightAmount = "15000"
pspShippingDetails.GiftMessage = "Happy Birthday!"
pspShippingDetails.GiftWrapping = "1"

PrimaryRecipient := nps.NewPrimaryRecipientStruct()
PrimaryRecipient.DateOfBirth = "1979-01-12"
PrimaryRecipient.FirstName = "John"
PrimaryRecipient.Gender = "M"
PrimaryRecipient.IDNumber = "54111111"
PrimaryRecipient.IDType = "200"
PrimaryRecipient.LastName = "Doe"
PrimaryRecipient.MiddleName = "Michael"
PrimaryRecipient.Nationality = "ARG"
PrimaryRecipient.PhoneNumber1 = "+1 011 11111111"
PrimaryRecipient.PhoneNumber2 = "+1 011 22222222"

pspShippingDetails.PrimaryRecipient = PrimaryRecipient

SecondaryRecipient := nps.NewSecondaryRecipientStruct()
SecondaryRecipient.DateOfBirth = "1979-01-12"
SecondaryRecipient.FirstName = "John"
SecondaryRecipient.Gender = "M"
SecondaryRecipient.IDNumber = "54111111"
SecondaryRecipient.IDType = "200"
SecondaryRecipient.LastName = "Doe"
SecondaryRecipient.MiddleName = "Michael"
SecondaryRecipient.Nationality = "ARG"
SecondaryRecipient.PhoneNumber1 = "+1 011 11111111"
SecondaryRecipient.PhoneNumber2 = "+1 011 22222222"

pspShippingDetails.SecondaryRecipient = SecondaryRecipient

Address := nps.NewAddressStruct()
Address.AdditionalInfo = "2 A"
Address.City = "Miami"
Address.Country = "USA"
Address.HouseNumber = "1245"
Address.StateProvince = "Florida"
Address.Street = "Av. Collins"
Address.ZipCode = "33140"

pspShippingDetails.Address = Address

SplitPayOnLine3p.psp_ShippingDetails = pspShippingDetails

pspTransactions := nps.NewArrayOf_TransactionsStruct()
pspTransactions.Items = make([]*nps.NewTransactionsStruct(), 0)

pspTransactions1 := nps.NewpspTransactionsStruct()
pspTransactions1.Psp_MerchantId = "sdk_test"
pspTransactions1.Psp_MerchTxRef = "ORDER66666-3"
pspTransactions1.Psp_Product = "14"
pspTransactions1.Psp_Amount = "10000"
pspTransactions1.Psp_NumPayments = "1"
pspTransactions.Items = append(pspTransactions.Items, pspTransactions1)

pspTransactions2 := nps.NewpspTransactionsStruct()
pspTransactions2.Psp_MerchantId = "sdk_test"
pspTransactions2.Psp_MerchTxRef = "ORDER66666-3"
pspTransactions2.Psp_Product = "14"
pspTransactions2.Psp_Amount = "5050"
pspTransactions2.Psp_NumPayments = "1"
pspTransactions.Items = append(pspTransactions.Items, pspTransactions2)


resp, err := service.SplitPayOnLine_3p(SplitPayOnLine3p)

if err != nil {
    fmt.Printf("Error: = [%s]", err)
}
fmt.Printf("Response = [%s] [%s]", resp.Psp_ResponseCod, resp.Psp_ResponseMsg)
fmt.Printf("Extended = [%s]", resp.Psp_ResponseExtended)
