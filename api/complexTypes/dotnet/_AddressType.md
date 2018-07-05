using System;
using NpsSDK;

ComplexElement Address = response.GetComplexElement("Address");

address.GetValue("AdditionalInfo");
address.GetValue("City");
address.GetValue("Country");
address.GetValue("HouseNumber");
address.GetValue("StateProvince");
address.GetValue("Street");
address.GetValue("ZipCode");
