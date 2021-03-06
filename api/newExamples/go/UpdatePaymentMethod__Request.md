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

UpdatePaymentMethod := npsSdk.NewRequerimientoStruct_UpdatePaymentMethod()

UpdatePaymentMethod.Psp_Version = "2.2"
UpdatePaymentMethod.Psp_MerchantId = "sdk_test"
UpdatePaymentMethod.Psp_PaymentMethodId = "Nzmd7DyGytXXC5PtKwnCsXXuQWHJB9EE"
UpdatePaymentMethod.Psp_PaymentMethodTag = "Corporate card"

pspCardInputDetails := nps.NewCardInputDetailsStruct()
pspCardInputDetails.ExpirationDate = "2501"

UpdatePaymentMethod.psp_CardInputDetails = pspCardInputDetails
UpdatePaymentMethod.Psp_PosDateTime = "2008-01-12 13:05:00"

resp, err := service.UpdatePaymentMethod(UpdatePaymentMethod)

if err != nil {
    fmt.Printf("Error: = [%s]", err)
}
fmt.Printf("Response = [%s] [%s]", resp.Psp_ResponseCod, resp.Psp_ResponseMsg)
fmt.Printf("Extended = [%s]", resp.Psp_ResponseExtended)
