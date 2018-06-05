local nps = require("npssdk")
nps.configuration.environment= nps.SANDBOX_ENV
nps.configuration.secret_key = "_YOUR_SECRET_KEY_"


updatecustomer = {}

updatecustomer.psp_Version = "2.2"
updatecustomer.psp_MerchantId = "sdk_test"
updatecustomer.psp_CustomerId = "bMnVPbNgX55oUz1VLgC41E5iD2rYRo2b"
updatecustomer.psp_EmailAddress = "jhon.doe@example.com"
updatecustomer.psp_AlternativeEmailAddress = "jdoe@example.com"
updatecustomer.psp_AccountCreatedAt = "2010-10-23"
updatecustomer.psp_AccountID = "jdoe78"

pspPaymentMethod = {}

CardInputDetails = {}
CardInputDetails.Number = "4507990000000010"
CardInputDetails.ExpirationDate = "2501"
CardInputDetails.SecurityCode = "123"
CardInputDetails.HolderName = "JOHN DOE"

pspPaymentMethod.CardInputDetails = CardInputDetails

updatecustomer.psp_PaymentMethod = pspPaymentMethod
updatecustomer.psp_PosDateTime = "2008-01-12 13:05:00"

response = nps.update_customer(updatecustomer)

print(resp.psp_ResponseCod)
