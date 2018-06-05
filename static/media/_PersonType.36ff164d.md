import NpsSDK.NpsSdk;
import NpsSDK.RootElement;
import NpsSDK.ComplexElement;
import NpsSDK.ComplexElementArray;
import NpsSDK.ComplexElementArrayItem;

ComplexElement person = response.getComplexElement("Person");


ComplexElement pspPerson = person.getComplexElement("psp_Person");
pspPerson.getValue("DateOfBirth");
pspPerson.getValue("FirstName");
pspPerson.getValue("Gender");
pspPerson.getValue("IDNumber");
pspPerson.getValue("IDType");
pspPerson.getValue("LastName");
pspPerson.getValue("MiddleName");
pspPerson.getValue("Nationality");
pspPerson.getValue("PhoneNumber1");
pspPerson.getValue("PhoneNumber2");

