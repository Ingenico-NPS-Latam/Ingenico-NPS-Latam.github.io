require_relative 'lib/nps_sdk'

conf = Nps::Configuration.new
conf.environment =Nps::Environments::STAGING_ENV
conf.key = "_YOUR_SECRET_KEY_"

npssdk = Nps::Sdk.new(conf)

params = {
    'psp_Version' => '2.2',
    'psp_MerchantId' => 'sdk_test',
    'psp_CustomerId' => 'bMnVPbNgX55oUz1VLgC41E5iD2rYRo2b',
    'psp_EmailAddress' => 'jhon.doe@example.com',
    'psp_AlternativeEmailAddress' => 'jdoe@example.com',
    'psp_AccountCreatedAt' => '2010-10-23',
    'psp_AccountID' => 'jdoe78',
    'psp_Person'  => {
        'FirstName' => 'John',
        'LastName' => 'Doe',
        'MiddleName' => 'Michael',
        'PhoneNumber1' => '+1 011 11111111',
        'PhoneNumber2' => '+1 011 22222222',
        'Gender' => 'M',
        'DateOfBirth' => '1979-01-12',
        'Nationality' => 'ARG',
        'IDNumber' => '54111111',
        'IDType' => '200'
    },
    'psp_Address'  => {
        'Street' => 'Av. Collins',
        'HouseNumber' => '1245',
        'AdditionalInfo' => '2 A',
        'City' => 'Miami',
        'StateProvince' => 'Florida',
        'Country' => 'USA',
        'ZipCode' => '33140'
    },
    'psp_PaymentMethod'  => {
        'CardInputDetails'  => {
            'Number' => '4507990000000010',
            'ExpirationDate' => '2501',
            'SecurityCode' => '123',
            'HolderName' => 'JOHN DOE'
            },
        'Person'  => {
            'FirstName' => 'John',
            'LastName' => 'Doe',
            'MiddleName' => 'Michael',
            'PhoneNumber1' => '+1 011 11111111',
            'PhoneNumber2' => '+1 011 22222222',
            'Gender' => 'M',
            'DateOfBirth' => '1979-01-12',
            'Nationality' => 'ARG',
            'IDNumber' => '54111111',
            'IDType' => '200'
            },
        'Address'  => {
            'Street' => 'Av. Collins',
            'HouseNumber' => '1245',
            'AdditionalInfo' => '2 A',
            'City' => 'Miami',
            'StateProvince' => 'Florida',
            'Country' => 'USA',
            'ZipCode' => '33140'
            }
    },
    'psp_PosDateTime' => '2008-01-12 13:05:00'
}

begin 
    response = npssdk.update_customer(params) 
rescue => e 
    puts e.message 
end 
