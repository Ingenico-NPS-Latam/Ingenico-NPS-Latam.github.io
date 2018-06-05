local nps = require("npssdk")
nps.configuration.environment= nps.SANDBOX_ENV
nps.configuration.secret_key = "_YOUR_SECRET_KEY_"


createcustomer = {}

createcustomer.psp_Version = "2.2"
createcustomer.psp_MerchantId = "sdk_test"
createcustomer.psp_EmailAddress = "jhon.doe@example.com"
createcustomer.psp_AlternativeEmailAddress = "jdoe@example.com"
createcustomer.psp_AccountID = "jdoe78"
createcustomer.psp_AccountCreatedAt = "2010-10-23"

pspPaymentMethod = {}

CardInputDetails = {}
CardInputDetails.Number = "4507990000000010"
CardInputDetails.ExpirationDate = "2501"
CardInputDetails.SecurityCode = "123"
CardInputDetails.HolderName = "JOHN DOE"

pspPaymentMethod.CardInputDetails = CardInputDetails

createcustomer.psp_PaymentMethod = pspPaymentMethod
createcustomer.psp_PosDateTime = "2008-01-12 13:05:00"

response = nps.create_customer(createcustomer)

print(resp.psp_ResponseCod)
