# Getting Started with Chimoney API

## Base URL
https://api-v2-sandbox.chimoney.io/v0.2.4

## Authentication
- Chimoney uses API Key authentication.
- Obtain your API key from your Chimoney dashboard.
- Add it to your request headers:


## Sample CURL Request
1. POST: Payout Airtime to a Phone number.

curl --request POST \
     --url https://api-v2-sandbox.chimoney.io/v0.2.4/payouts/airtime \
     --header 'X-API-KEY: 2280d6148a3766ec2be0b5a1315bb5a1be35ef6f21f95d698a258210fa92b572' \
     --header 'accept: application/json' \
     --header 'content-type: application/json' \
     --data '
{
  "airtimes": [
    {
      "countryToSend": "Nigeria",
      "phoneNumber": "08105204229",
      "valueInUSD": "10"
    }
  ]
}
'

RESPONSE
{
  "status": "error",
  "type": "Transaction Error",
  "code": "TRANSACTION_FAILED",
  "message": "fail to send bulk airtime"
}

2. Get list of all supported mobile money codes.

CURL REQUEST

curl --request GET \
     --url https://api-v2-sandbox.chimoney.io/v0.2.4/info/mobile-money-codes \
     --header 'X-API-KEY: 2280d6148a3766ec2be0b5a1315bb5a1be35ef6f21f95d698a258210fa92b572' \
     --header 'accept: application/json'

RESPONSE

{
  "status": "success",
  "message": "Supported mobile money code retrieved successfully",
  "data": [
    {
      "name": "Cameroon YUP",
      "country": "Cameroon",
      "code": "YUP",
      "provider": "flw",
      "manual": true
    },
    {
      "name": "Cameroon UBC",
      "country": "Cameroon",
      "code": "UBC",
      "provider": "flw",
      "manual": true
    },
    {
      "name": "Cameroon ORANGEMONEY",
      "country": "Cameroon",
      "code": "ORANGEMONEY",
      "provider": "flw",
      "manual": true
    },
    {
      "name": "Cameroon MTN",
      "country": "Cameroon",
      "code": "MTN",
      "provider": "flw",
      "manual": true
    },
    {
      "name": "Cameroon LAREGIONALE",
      "country": "Cameroon",
      "code": "LAREGIONALE",
      "provider": "flw",
      "manual": true
    },
    {
      "name": "Cameroon EUMOBILE",
      "country": "Cameroon",
      "code": "EUMOBILE",
      "provider": "flw",
      "manual": true
    },
    {
      "name": "Cameroon CCA",
      "country": "Cameroon",
      "code": "CCA",
      "provider": "flw",
      "manual": true
    },
    {
      "name": "Cameroon CBC",
      "country": "Cameroon",
      "code": "CBC",
      "provider": "flw",
      "manual": true
    },
    {
      "name": "Cameroon BICEC",
      "country": "Cameroon",
      "code": "BICEC",
      "provider": "flw",
      "manual": true
    },
    {
      "name": "Chad MooV",
      "country": "Chad",
      "code": "MOOV",
      "provider": "flw",
      "manual": true
    },
    {
      "name": "Chad Airtel",
      "country": "Chad",
      "code": "AIRTEL",
      "provider": "flw",
      "manual": true
    },
    {
      "name": "Cote d'Ivoire WAVE",
      "country": "Cote d'Ivoire",
      "code": "WAVE",
      "provider": "flw",
      "manual": true
    },
    {
      "name": "Cote d'Ivoire ORANGEMONEY",
      "country": "Cote d'Ivoire",
      "code": "ORANGEMONEY",
      "provider": "flw",
      "manual": true
    },
    {
      "name": "Cote d'Ivoire MTN",
      "country": "Cote d'Ivoire",
      "code": "MTN",
      "provider": "flw",
      "manual": true
    },
    {
      "name": "Cote d'Ivoire MOOVE",
      "country": "Cote d'Ivoire",
      "code": "MOOVE",
      "provider": "flw",
      "manual": true
    },
    {
      "name": "Cote d'Ivoire FMM",
      "country": "Cote d'Ivoire",
      "code": "FMM",
      "provider": "flw",
      "manual": true
    },
    {
      "name": "Equatorial Guinea ORANGE",
      "country": "Equatorial Guinea",
      "code": "ORANGE",
      "provider": "flw",
      "manual": true
    },
    {
      "name": "Equatorial Guinea MTN",
      "country": "Equatorial Guinea",
      "code": "MTN",
      "provider": "flw",
      "manual": true
    },
    {
      "name": "Gabon ORANGE",
      "country": "Gabon",
      "code": "ORANGE",
      "provider": "flw",
      "manual": true
    },
    {
      "name": "Gabon BGFI",
      "country": "Gabon",
      "code": "BGFI",
      "provider": "flw",
      "manual": true
    },
    {
      "name": "Gabon MTN",
      "country": "Gabon",
      "code": "MTN",
      "provider": "flw",
      "manual": true
    },
    {
      "name": "Ghana VODAFONE",
      "country": "Ghana",
      "code": "VODAFONE",
      "provider": "flw",
      "manual": false
    },
    {
      "name": "Ghana MTN",
      "country": "Ghana",
      "code": "MTN",
      "provider": "flw",
      "manual": false
    },
    {
      "name": "Ghana AIRTEL-TIGO",
      "country": "Ghana",
      "code": "AIRTEL-TIGO",
      "provider": "flw",
      "manual": false
    },
    {
      "name": "Kenya M-Pesa",
      "country": "Kenya",
      "code": "MPS",
      "provider": "flw",
      "manual": false
    },
    {
      "name": "Malawi AIRTEL",
      "country": "Malawi",
      "code": "AIRTEL",
      "provider": "flw",
      "manual": true
    },
    {
      "name": "Republic of Congo ORANGE",
      "country": "Republic of Congo",
      "code": "ORANGE",
      "provider": "flw",
      "manual": true
    },
    {
      "name": "Republic of Congo BGFI",
      "country": "Republic of Congo",
      "code": "BGFI",
      "provider": "flw",
      "manual": true
    },
    {
      "name": "Republic of Congo MTN",
      "country": "Republic of Congo",
      "code": "MTN",
      "provider": "flw",
      "manual": true
    },
    {
      "name": "Rwanda MTN",
      "country": "Rwanda",
      "code": "MTN",
      "provider": "flw",
      "manual": true
    },
    {
      "name": "Rwanda AIRTEL",
      "country": "Rwanda",
      "code": "AIRTEL",
      "provider": "flw",
      "manual": true
    },
    {
      "name": "Senegal WAVE",
      "country": "Senegal",
      "code": "WAVE",
      "provider": "flw",
      "manual": true
    },
    {
      "name": "Senegal ORANGEMONEY",
      "country": "Senegal",
      "code": "ORANGEMONEY",
      "provider": "flw",
      "manual": true
    },
    {
      "name": "Senegal FREEMONEY",
      "country": "Senegal",
      "code": "FREEMONEY",
      "provider": "flw",
      "manual": true
    },
    {
      "name": "Tanzania VODACOM",
      "country": "Tanzania",
      "code": "VODACOM",
      "provider": "flw",
      "manual": true
    },
    {
      "name": "Tanzania MPS",
      "country": "Tanzania",
      "code": "MPS",
      "provider": "flw",
      "manual": true
    },
    {
      "name": "Tanzania TIGO",
      "country": "Tanzania",
      "code": "TIGO",
      "provider": "flw",
      "manual": true
    },
    {
      "name": "Tanzania HALOPESA",
      "country": "Tanzania",
      "code": "HALOPESA",
      "provider": "flw",
      "manual": true
    },
    {
      "name": "Tanzania AIRTEL",
      "country": "Tanzania",
      "code": "AIRTEL",
      "provider": "flw",
      "manual": true
    },
    {
      "name": "Tanzania VODACOM",
      "country": "Tanzania",
      "code": "VODACOM",
      "provider": "flw",
      "manual": true
    },
    {
      "name": "Tanzania MPS",
      "country": "Tanzania",
      "code": "MPS",
      "provider": "flw",
      "manual": true
    },
    {
      "name": "Tanzania TIGO",
      "country": "Tanzania",
      "code": "TIGO",
      "provider": "flw",
      "manual": true
    },
    {
      "name": "Tanzania HALOPESA",
      "country": "Tanzania",
      "code": "HALOPESA",
      "provider": "flw",
      "manual": true
    },
    {
      "name": "Tanzania AIRTEL",
      "country": "Tanzania",
      "code": "AIRTEL",
      "provider": "flw",
      "manual": true
    },
    {
      "name": "Uganda Airtel",
      "country": "Uganda",
      "code": "AIRTEL",
      "provider": "flw",
      "manual": true
    },
    {
      "name": "Uganda MTN",
      "country": "Uganda",
      "code": "MTN",
      "provider": "flw",
      "manual": false
    },
    {
      "name": "Zambia ZAMTEL",
      "country": "Zambia",
      "code": "ZAMTEL",
      "provider": "flw",
      "manual": true
    },
    {
      "name": "Zambia MTN",
      "country": "Zambia",
      "code": "MTN",
      "provider": "flw",
      "manual": true
    },
    {
      "name": "Zambia AIRTEL",
      "country": "Zambia",
      "code": "AIRTEL",
      "provider": "flw",
      "manual": true
    }
  ]
}