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

BankPayment3p := npsSdk.NewRequerimientoStruct_BankPayment_3p()

BankPayment3p.Psp_Version = "2.2"
BankPayment3p.Psp_MerchantId = "sdk_test"
BankPayment3p.Psp_TxSource = "WEB"
BankPayment3p.Psp_MerchTxRef = "ORDER66666-3"
BankPayment3p.Psp_MerchOrderId = "ORDER66666"
BankPayment3p.Psp_ReturnURL = "http://localhost/"
BankPayment3p.Psp_FrmLanguage = "es_AR"
BankPayment3p.Psp_ScreenDescription = "Descripcion"
BankPayment3p.Psp_TicketDescription = "Descripcion"
BankPayment3p.Psp_Currency = "032"
BankPayment3p.Psp_Country = "ARG"
BankPayment3p.Psp_Product = "320"
BankPayment3p.Psp_ExpDate1 = "2019-12-01"
BankPayment3p.Psp_Amount1 = "15050"
BankPayment3p.Psp_ExpMark = "0"
BankPayment3p.Psp_ExpTime = "14:00:00"
BankPayment3p.Psp_PosDateTime = "2019-12-01 12:00:00"

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

BankPayment3p.psp_CustomerAdditionalDetails = pspCustomerAdditionalDetails

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

BankPayment3p.psp_BillingDetails = pspBillingDetails

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

BankPayment3p.psp_ShippingDetails = pspShippingDetails

pspOrderDetails := nps.NewOrderDetailsStruct()

OrderItems := nps.NewArrayOf_OrderItemsStruct()
OrderItems.Items = make([]*nps.NewOrderItemsStruct(), 0)

OrderItems1 := nps.NewOrderItemsStruct()
OrderItems1.Quantity = "10"
OrderItems1.UnitPrice = "10050"
OrderItems1.Description = "Blue pencil"
OrderItems1.Type = "1002"
OrderItems1.SkuCode = "SO-4587885545"
OrderItems1.ManufacturerPartNumber = "CN-0N2828421-3AD-02CD"
OrderItems1.Risk = "H"
OrderItems.Items = append(OrderItems.Items, OrderItems1)


BankPayment3p.psp_OrderDetails = pspOrderDetails

resp, err := service.BankPayment_3p(BankPayment3p)

if err != nil {
    fmt.Printf("Error: = [%s]", err)
}
fmt.Printf("Response = [%s] [%s]", resp.Psp_ResponseCod, resp.Psp_ResponseMsg)
fmt.Printf("Extended = [%s]", resp.Psp_ResponseExtended)
