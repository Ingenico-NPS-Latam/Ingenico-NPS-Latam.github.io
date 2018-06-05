require_relative 'lib/nps_sdk'

conf = Nps::Configuration.new
conf.environment =Nps::Environments::STAGING_ENV
conf.key = "_YOUR_SECRET_KEY_"

npssdk = Nps::Sdk.new(conf)

params = {
    'psp_Version' => '2.2',
    'psp_MerchantId' => 'sdk_test',
    'psp_PaymentMethodId' => 'Nzmd7DyGytXXC5PtKwnCsXXuQWHJB9EE',
    'psp_PaymentMethodTag' => 'Corporate card',
    'psp_CardInputDetails'  => {
        'ExpirationDate' => '2501',
        'HolderName' => 'JOHN DOE'
    },
    'psp_Person'  => {
        'FirstName' => 'John',
        'LastName' => 'Doe',
        'MiddleName' => 'Michael',
        'PhoneNumber1' => '+1 011 11111111',
        'PhoneNumber2' => '+1 011 22222222',
        'DateOfBirth' => '1979-01-12',
        'Nationality' => 'ARG',
        'Gender' => 'M',
        'IDNumber' => '54111111',
        'IDType' => '200'
    },
    'psp_Address'  => {
        'Street' => 'Av. Collins',
        'HouseNumber' => '4702',
        'AdditionalInfo' => '2 A',
        'StateProvince' => 'CABA',
        'City' => 'Buenos Aires',
        'Country' => 'ARG',
        'ZipCode' => '1425'
    },
    'psp_PosDateTime' => '2008-01-12 13:05:00'
}

begin 
    response = npssdk.update_payment_method(params) 
rescue => e 
    puts e.message 
end 
