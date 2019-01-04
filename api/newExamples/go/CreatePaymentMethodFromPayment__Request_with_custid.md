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

CreatePaymentMethodFromPayment := npsSdk.NewRequerimientoStruct_CreatePaymentMethodFromPayment()

CreatePaymentMethodFromPayment.Psp_Version = "2.2"
CreatePaymentMethodFromPayment.Psp_MerchantId = "sdk_test"
CreatePaymentMethodFromPayment.Psp_TransactionId = "65340022"
CreatePaymentMethodFromPayment.Psp_PaymentMethodTag = "Corporate card"
CreatePaymentMethodFromPayment.Psp_CustomerId = "bMnVPbNgX55oUz1VLgC41E5iD2rYRo2b"
CreatePaymentMethodFromPayment.Psp_SetAsCustomerDefault = "1"
CreatePaymentMethodFromPayment.Psp_PosDateTime = "2008-01-12 13:05:00"

resp, err := service.CreatePaymentMethodFromPayment(CreatePaymentMethodFromPayment)

if err != nil {
    fmt.Printf("Error: = [%s]", err)
}
fmt.Printf("Response = [%s] [%s]", resp.Psp_ResponseCod, resp.Psp_ResponseMsg)
fmt.Printf("Extended = [%s]", resp.Psp_ResponseExtended)
