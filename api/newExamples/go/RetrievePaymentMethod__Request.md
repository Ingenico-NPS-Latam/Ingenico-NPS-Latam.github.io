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

RetrievePaymentMethod := npsSdk.NewRequerimientoStruct_RetrievePaymentMethod()

RetrievePaymentMethod.Psp_Version = "2.2"
RetrievePaymentMethod.Psp_MerchantId = "sdk_test"
RetrievePaymentMethod.Psp_PaymentMethodId = "jGW24iDaoMBzfKHViL18TmHo9sHBgW4J"
RetrievePaymentMethod.Psp_PosDateTime = "2008-01-12 13:05:00"

resp, err := service.RetrievePaymentMethod(RetrievePaymentMethod)

if err != nil {
    fmt.Printf("Error: = [%s]", err)
}
fmt.Printf("Response = [%s] [%s]", resp.Psp_ResponseCod, resp.Psp_ResponseMsg)
fmt.Printf("Extended = [%s]", resp.Psp_ResponseExtended)
