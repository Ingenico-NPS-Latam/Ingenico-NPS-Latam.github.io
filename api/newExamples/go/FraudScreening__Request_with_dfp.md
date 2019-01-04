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

FraudScreening := npsSdk.NewRequerimientoStruct_FraudScreening()

FraudScreening.Psp_Version = "2.2"
FraudScreening.Psp_MerchantId = "sdk_test"
FraudScreening.Psp_TxSource = "WEB"
FraudScreening.Psp_MerchTxRef = "ORDER66666-3"
FraudScreening.Psp_MerchOrderId = "ORDER66666"
FraudScreening.Psp_Amount = "15050"
FraudScreening.Psp_NumPayments = "1"
FraudScreening.Psp_Currency = "032"
FraudScreening.Psp_Country = "ARG"
FraudScreening.Psp_Product = "14"
FraudScreening.Psp_CardNumber = "4507990000000010"
FraudScreening.Psp_CardExpDate = "1912"
FraudScreening.Psp_PosDateTime = "2019-12-01 12:00:00"

pspCustomerAdditionalDetails := nps.NewCustomerAdditionalDetailsStruct()
pspCustomerAdditionalDetails.DeviceFingerPrint = "KJhKHKJgh7777kgh..."

FraudScreening.psp_CustomerAdditionalDetails = pspCustomerAdditionalDetails

resp, err := service.FraudScreening(FraudScreening)

if err != nil {
    fmt.Printf("Error: = [%s]", err)
}
fmt.Printf("Response = [%s] [%s]", resp.Psp_ResponseCod, resp.Psp_ResponseMsg)
fmt.Printf("Extended = [%s]", resp.Psp_ResponseExtended)
