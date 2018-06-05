import NpsSDK.NpsSdk;
import NpsSDK.RootElement;
import NpsSDK.ComplexElement;
import NpsSDK.ComplexElementArray;
import NpsSDK.ComplexElementArrayItem;

ComplexElement billingDetails = response.getComplexElement("BillingDetails");

billingDetails.getValue("Invoice");
billingDetails.getValue("InvoiceDate");
billingDetails.getValue("InvoiceAmount");
billingDetails.getValue("InvoiceCurrency");

ComplexElement person = billingDetails.getComplexElement("Person");
person.getValue("DateOfBirth");
person.getValue("FirstName");
person.getValue("Gender");
person.getValue("IDNumber");
person.getValue("IDType");
person.getValue("LastName");
person.getValue("MiddleName");
person.getValue("Nationality");
person.getValue("PhoneNumber1");
person.getValue("PhoneNumber2");


ComplexElement address = billingDetails.getComplexElement("Address");
address.getValue("AdditionalInfo");
address.getValue("City");
address.getValue("Country");
address.getValue("HouseNumber");
address.getValue("StateProvince");
address.getValue("Street");
address.getValue("ZipCode");

