package main

import (
        "fmt"
        "log"
        "npsSdk"
        CONSTANTS "npsSdk/constants"
)

service:= nps.NewPaymentServicePlatformPortType(true)

amountDetailsRequestType.md := nps.NewRequerimientoStruct_AmountDetailsRequestType.md()


AmountDetailsRequest := nps.NewAmountDetailsRequestStruct()
AmountDetailsRequest.Tip = "500"
AmountDetailsRequest.Discount = "10000"

    ComplexElementArray Taxes = new ComplexElementArray();

    ComplexElementArrayItem Taxes1 = new ComplexElementArrayItem();
Taxes1.TypeId = "500"
Taxes1.Amount = "10000"
Taxes1.Rate = "2100"
Taxes1.BaseAmount = "10000"

    Taxes.add(Taxes1);

    ComplexElementArrayItem Taxes2 = new ComplexElementArrayItem();
Taxes2.TypeId = "500"
Taxes2.Amount = "10000"
Taxes2.Rate = "2100"
Taxes2.BaseAmount = "10000"

    Taxes.add(Taxes2);

AmountDetailsRequest.Taxes = Taxes

amountDetailsRequestType.md.AmountDetailsRequest = AmountDetailsRequest

resp, err := service.AmountDetailsRequestType.md(amountDetailsRequestType.md)

if err != nil {
    fmt.Printf("Error: = [%s]", err)
}
fmt.Printf("Response = [%s] [%s]", resp.Psp_ResponseCod, resp.Psp_ResponseMsg)
fmt.Printf("Extended = [%s]", resp.Psp_ResponseExtended)