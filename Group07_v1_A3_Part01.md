## API Description

Construction Under Manitoba API (CUMAPI) is designed to provide current and upcoming Manitoba road construction information based on neighbourhoods, cities, or the province as a whole. The user will send their desired date to CUMAPI and receive road construction information relevant to the given date. 

## Endpoints and Parameters

1. By Neighbourhood
  https://cumapi.com/neighbourhood/{yyyy-mm-dd}
2. By City
  https://cumapi.com/city/{yyyy-mm-dd}
3. All of Manitoba
  https://cumapi.com/manitoba/{yyyy-mm-dd}

## Description of Resources
When using the Neighbourhood endpoint the user will recieve all streets with construction sorted by neighbourhood
{
"neighbourhood": [
  {
    neighbourhood name: neighbourhood name,
    "street": [
       {
         "street name": "name of street",
         "direction": "cardinal direction",
         "lane(s)": "lane with construction"
       }
      ]
    }
  ]
}

When using the City endpoint the user will recieve all streets with construction sorted by city


When using the Manitoba endpoint the user will recieve all streets with construction in Manitoba
{
  "manitoba": {
  "street": [
    {
      "street name": "name of street",
      "direction": "cardinal direction",
      "lane(s)": "lane with construction"
    }
    ]
  } 
}

## Sample Request and Response
the actual sent back response and request
https://cumapi.com/neighbourhood/{yyyy-mm-dd}?yyyy-mm-dd=2022-4-1

{
"neighbourhood": [
  {
    "neighbourhood name": "Winnipeg North",
    "street": [
       {
         "streetname": "Main Street",
         "direction": "North",
         "lane(s)": "Middle, right"
       },
       {
         "street name": "Leila Avenue",
         "direction": "East",
         "lane(s)": "Left"
       }
      ]
    }
  ]
}
