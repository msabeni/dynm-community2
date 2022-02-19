---
title: DYNM COMMUNITY

language_tabs: # must be one of https://git.io/vQNgJ
  - shell: cURL
  - javascript: Javascript
  - python: Python
  - php: PHP

toc_footers:
  - <a href='https://github.com/slatedocs/slate'>Documentation Powered by Slate</a>

includes:
  - errors

search: true

code_clipboard: true
---

# Introduction

HOST: [https://dynm.herokuapp.com/](https://dynm.herokuapp.com/).

## About

Dynmhx Community is designed to support cities in reporting city-wide GHG emissions according to GPC protocol.

# Community Stationary Combustion

> REQUEST

```shell
curl --location --request POST 'https://dynm-corporate.herokuapp.com/community/stationary-combustion' \
--header 'Content-Type: application/json' \
--data-raw '{
    "gpc_ref": "I.1.1",
    "scope": "1",
    "description": "Stationary Emissions for Biodiesels fuel type",
    "activity": "Biodiesels",
    "category": "I.1 RESIDENTIAL BUILDINGS",
    "sub_category": "Emissions from fuel combustion within the city boundary",
    "sub_category_option": "Residential (1.a.b)",
    "notation_key": "NO",
    "activity_amount": 1000,
    "activity_units": "kWh",
    "activity_multiplier_units": "kWh",
    "activity_multiplier": null,
    "oxidation_factor": 1,
    "gases": "CO2",
    "manual_emissions_data": false,
    "emission_factor": "Biodiesels EF",
    "CO2": null,
    "CH4": null,
    "total_CO2e": null,
    "CO2b": null,
    "N2O": null,
    "data_quality": "L",
    "methodology_description": "",
    "source": "",
    "data_quality_explanation": "",
    "custom_emission_factors": [
        {
            "activity": "Biodiesels",
            "reference": "Biodiesels EF",
            "type": "GHG",
            "gwp": "4AR",
            "unit_numerator": "kg",
            "unit_denominator": "kWh",
            "CO2": 1000,
            "CH4": 100,
            "N2O": 100,
            "total_CO2e": 1000,
            "CO2b": 100,
            "data_quality": "",
            "year": 2019,
            "scale": "",
            "description": "",
            "source": ""
        }
    ]
}'

```

```javascript
import fetch from "node-fetch";
const data = {
  gpc_ref: "I.1.1",
  scope: "1",
  description: "Stationary Emissions for Biodiesels fuel type",
  activity: "Biodiesels",
  category: "I.1 RESIDENTIAL BUILDINGS",
  sub_category: "Emissions from fuel combustion within the city boundary",
  sub_category_option: "Residential (1.a.b)",
  notation_key: "NO",
  activity_amount: 1000,
  activity_units: "kWh",
  activity_multiplier_units: "kWh",
  activity_multiplier: null,
  oxidation_factor: 1,
  gases: "CO2",
  manual_emissions_data: false,
  emission_factor: "Biodiesels EF",
  CO2: null,
  CH4: null,
  total_CO2e: null,
  CO2b: null,
  N2O: null,
  data_quality: "L",
  methodology_description: "",
  source: "",
  data_quality_explanation: "",
  custom_emission_factors: [
    {
      activity: "Biodiesels",
      reference: "Biodiesels EF",
      type: "GHG",
      gwp: "4AR",
      unit_numerator: "kg",
      unit_denominator: "kWh",
      CO2: 1000,
      CH4: 100,
      N2O: 100,
      total_CO2e: 1000,
      CO2b: 100,
      data_quality: "",
      year: 2019,
      scale: "",
      description: "",
      source: "",
    },
  ],
};

fetch("https://dynm-corporate.herokuapp.com/community/stationary-combustion", {
  method: "POST",
  headers: {
    "Content-Type": "application/json",
  },
  body: JSON.stringify(data),
})
  .then((response) => response.json())
  .then((data) => {
    console.log("Success:", data);
  })
  .catch((error) => {
    console.error("Error:", error);
  });
```

```python
import requests
import json

url = "https://dynm-corporate.herokuapp.com/community/stationary-combustion"

payload = json.dumps({
  "gpc_ref": "I.1.1",
  "scope": "1",
  "description": "Stationary Emissions for Biodiesels fuel type",
  "activity": "Biodiesels",
  "category": "I.1 RESIDENTIAL BUILDINGS",
  "sub_category": "Emissions from fuel combustion within the city boundary",
  "sub_category_option": "Residential (1.a.b)",
  "notation_key": "NO",
  "activity_amount": 1000,
  "activity_units": "kWh",
  "activity_multiplier_units": "kWh",
  "activity_multiplier": None,
  "oxidation_factor": 1,
  "gases": "CO2",
  "manual_emissions_data": False,
  "emission_factor": "Biodiesels EF",
  "CO2": None,
  "CH4": None,
  "total_CO2e": None,
  "CO2b": None,
  "N2O": None,
  "data_quality": "L",
  "methodology_description": "",
  "source": "",
  "data_quality_explanation": "",
  "custom_emission_factors": [
    {
      "activity": "Biodiesels",
      "reference": "Biodiesels EF",
      "type": "GHG",
      "gwp": "4AR",
      "unit_numerator": "kg",
      "unit_denominator": "kWh",
      "CO2": 1000,
      "CH4": 100,
      "N2O": 100,
      "total_CO2e": 1000,
      "CO2b": 100,
      "data_quality": "",
      "year": 2019,
      "scale": "",
      "description": "",
      "source": ""
    }
  ]
})
headers = {
  'Content-Type': 'application/json'
}

response = requests.request("POST", url, headers=headers, data=payload)

print(response.text)

```

```php
<?php

$curl = curl_init();

curl_setopt_array($curl, array(
  CURLOPT_URL => 'https://dynm-corporate.herokuapp.com/community/stationary-combustion',
  CURLOPT_RETURNTRANSFER => true,
  CURLOPT_ENCODING => '',
  CURLOPT_MAXREDIRS => 10,
  CURLOPT_TIMEOUT => 0,
  CURLOPT_FOLLOWLOCATION => true,
  CURLOPT_HTTP_VERSION => CURL_HTTP_VERSION_1_1,
  CURLOPT_CUSTOMREQUEST => 'POST',
  CURLOPT_POSTFIELDS =>'{
    "gpc_ref": "I.1.1",
    "scope": "1",
    "description": "Stationary Emissions for Biodiesels fuel type",
    "activity": "Biodiesels",
    "category": "I.1 RESIDENTIAL BUILDINGS",
    "sub_category": "Emissions from fuel combustion within the city boundary",
    "sub_category_option": "Residential (1.a.b)",
    "notation_key": "NO",
    "activity_amount": 1000,
    "activity_units": "kWh",
    "activity_multiplier_units": "kWh",
    "activity_multiplier": null,
    "oxidation_factor": 1,
    "gases": "CO2",
    "manual_emissions_data": false,
    "emission_factor": "Biodiesels EF",
    "CO2": null,
    "CH4": null,
    "total_CO2e": null,
    "CO2b": null,
    "N2O": null,
    "data_quality": "L",
    "methodology_description": "",
    "source": "",
    "data_quality_explanation": "",
    "custom_emission_factors": [
        {
            "activity": "Biodiesels",
            "reference": "Biodiesels EF",
            "type": "GHG",
            "gwp": "4AR",
            "unit_numerator": "kg",
            "unit_denominator": "kWh",
            "CO2": 1000,
            "CH4": 100,
            "N2O": 100,
            "total_CO2e": 1000,
            "CO2b": 100,
            "data_quality": "",
            "year": 2019,
            "scale": "",
            "description": "",
            "source": ""
        }
    ]
}',
  CURLOPT_HTTPHEADER => array(
    'Content-Type: application/json'
  ),
));

$response = curl_exec($curl);

curl_close($curl);
echo $response;

```

> RESPONSE : <code>200</code>

```json
{
  "CH4_tCO2e": 2500.0,
  "N20_tCO2e": 29799.999999999996,
  "TtCO2e": 1000.0,
  "tCO2b": 100.0,
  "tCO2e": 1000.0
}
```

Endpoint for recording activity and emissions data for Stationary energy sources.

`POST https://dynm-corporate.herokuapp.com/community/stationary-combustion`

<aside>Request params</aside>

| Param                     | Type    | Required | Description                                                                                                                                                                                             |
| ------------------------- | ------- | -------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| gpc_ref                   | string  | true     | The GPC reference string for this category e.g I.1.1 for the sub-category ‘Emissions from fuel combustion within the city boundary’ within Stationary Combustion’s category ‘I.1 RESIDENTIAL BUILDINGS’ |
| scope                     | string  | true     | The appropriate scope. One of 1, 2 or 3                                                                                                                                                                 |
| description               | string  | nullable | General description of the row activity or calculation.                                                                                                                                                 |
| activity                  | string  | true     | The emission type or activity being reported on e.g Biodiesels                                                                                                                                          |
| category                  | string  | true     | The emission type or activity being reported on e.g Biodiesels                                                                                                                                          |
| sub_category              | string  | nullable | Appropriate sub-category under Inventory options with sub-categories e.g from the gpc_ref example above Emissions from fuel combustion within the city boundary                                         |
| sub_category_option       | string  | nullable | Appropriate sub(sub-category) under Inventory options with sub-categories e.g from the gpc_ref example above Residential 1.A.4.b                                                                        |
| notation_key              | string  | true     | Denote justifications for exclusion or partial accounting of GHG emission source categories. E.g NE for Not Estimated                                                                                   |
| activity_amount           | float   | true     | Amount of the units of the selected activity to report on. eg 100                                                                                                                                       |
| activity_units            | string  | true     | Measurement units for the activity data e.g kWh                                                                                                                                                         |
| activity_multiplier_units | string  | nullable | Units to be used if you wish to convert your data e.g kWh                                                                                                                                               |
| activity_multiplier       | float   | nullabke | An override value for converting activity data. If provided the conversion from activity_multiplier_units won’t be used rather this figure will be used. E.g 1.0                                        |
| oxidation_factor          | float   | nullable | Overrides default oxidation factor(1) e.g 1.0                                                                                                                                                           |
| gases                     | string  | nullable | Selection of gases in the reported emissions                                                                                                                                                            |
| manual_emissions_data     | boolean | true     | Indicates whether to use manually entered emission data or to calculate from an emission dataset. Defaults to false.                                                                                    |
| emission_factor           | string  | nullable | Name of the custom emission factor to be referenced. It is the reference field from one of the custom emission factors added. e.g Biodiesels_EF                                                         |
| CO2                       | float   | nullable | Manually entered C02 emissions                                                                                                                                                                          |
| CH4                       | float   | nullable | Manually entered CH4 emissions                                                                                                                                                                          |
| total_CO2e                | float   | nullable | Manually entered total_CO2e emissions                                                                                                                                                                   |
| CO2b                      | float   | nullable | Manually entered CO2b emissions                                                                                                                                                                         |
| N2O                       | float   | nullable | Manually entered N2O emissions                                                                                                                                                                          |
| data_quality              | string  | true     | Denotes quality of the submitted emissions data e.g L                                                                                                                                                   |
| methodology_description   | string  | nullable | Description of the methodology used for selecting a Notation Key                                                                                                                                        |
| source                    | string  | true     | The data source for the emissions or activity.                                                                                                                                                          |
| data_quality_explanation  | string  | true     | The explanation for choice of data quality level.                                                                                                                                                       |
| custom_emission_factors   | list    | true     | custom params for this particular endpoint                                                                                                                                                              |

# Community Transportation

> REQUEST

```shell
curl --location --request POST 'https://dynm-corporate.herokuapp.com/community/transportation' \
--header 'Content-Type: application/json' \
--data-raw '{
    "gpc_ref": "II.1.1",
    "scope": "1",
    "fleet_type": "Municipal",
    "method": "Fuel sales approach",
    "description": "Stationary Emissions for Biodiesels fuel type",
    "activity": "Biodiesels",
    "category": "II.1 ON-ROAD TRANSPORTATION",
    "sub_category": "Emissions from fuel combustion on-road combustion ocurring in the city",
    "notation_key": "NO",
    "activity_amount": 1000,
    "activity_units": "kWh",
    "activity_multiplier_units": "kWh",
    "activity_multiplier": null,
    "oxidation_factor": 1,
    "gases": "CO2",
    "manual_emissions_data": false,
    "emission_factor": "Biodiesels EF",
    "CO2": null,
    "CH4": null,
    "total_CO2e": null,
    "CO2b": null,
    "N2O": null,
    "data_quality": "L",
    "methodology_description": "",
    "source": "",
    "data_quality_explanation": "",
    "custom_emission_factors": [
        {
            "activity": "Biodiesels",
            "reference": "Biodiesels EF",
            "type": "GHG",
            "gwp": "4AR",
            "unit_numerator": "kg",
            "unit_denominator": "kWh",
            "CO2": 1000,
            "CH4": 100,
            "N2O": 100,
            "total_CO2e": 1000,
            "CO2b": 100,
            "data_quality": "",
            "year": 2019,
            "scale": "",
            "description": "",
            "source": ""
        }
    ]
}'
```

```javascript
import fetch from "node-fetch";
const data = {
  gpc_ref: "II.1.1",
  scope: "1",
  fleet_type: "Municipal",
  method: "Fuel sales approach",
  description: "Stationary Emissions for Biodiesels fuel type",
  activity: "Biodiesels",
  category: "II.1 ON-ROAD TRANSPORTATION",
  sub_category:
    "Emissions from fuel combustion on-road combustion ocurring in the city",
  notation_key: "NO",
  activity_amount: 1000,
  activity_units: "kWh",
  activity_multiplier_units: "kWh",
  activity_multiplier: null,
  oxidation_factor: 1,
  gases: "CO2",
  manual_emissions_data: false,
  emission_factor: "Biodiesels EF",
  CO2: null,
  CH4: null,
  total_CO2e: null,
  CO2b: null,
  N2O: null,
  data_quality: "L",
  methodology_description: "",
  source: "",
  data_quality_explanation: "",
  custom_emission_factors: [
    {
      activity: "Biodiesels",
      reference: "Biodiesels EF",
      type: "GHG",
      gwp: "4AR",
      unit_numerator: "kg",
      unit_denominator: "kWh",
      CO2: 1000,
      CH4: 100,
      N2O: 100,
      total_CO2e: 1000,
      CO2b: 100,
      data_quality: "",
      year: 2019,
      scale: "",
      description: "",
      source: "",
    },
  ],
};

fetch("https://dynm-corporate.herokuapp.com/community/transportation", {
  method: "POST",
  headers: {
    "Content-Type": "application/json",
  },
  body: JSON.stringify(data),
})
  .then((response) => response.json())
  .then((data) => {
    console.log("Success:", data);
  })
  .catch((error) => {
    console.error("Error:", error);
  });
```

```python
import requests
import json

url = "https://dynm-corporate.herokuapp.com/community/transportation"

payload = json.dumps({
  "gpc_ref": "II.1.1",
  "scope": "1",
  "fleet_type": "Municipal",
  "method": "Fuel sales approach",
  "description": "Stationary Emissions for Biodiesels fuel type",
  "activity": "Biodiesels",
  "category": "II.1 ON-ROAD TRANSPORTATION",
  "sub_category": "Emissions from fuel combustion on-road combustion ocurring in the city",
  "notation_key": "NO",
  "activity_amount": 1000,
  "activity_units": "kWh",
  "activity_multiplier_units": "kWh",
  "activity_multiplier": None,
  "oxidation_factor": 1,
  "gases": "CO2",
  "manual_emissions_data": False,
  "emission_factor": "Biodiesels EF",
  "CO2": None,
  "CH4": None,
  "total_CO2e": None,
  "CO2b": None,
  "N2O": None,
  "data_quality": "L",
  "methodology_description": "",
  "source": "",
  "data_quality_explanation": "",
  "custom_emission_factors": [
    {
      "activity": "Biodiesels",
      "reference": "Biodiesels EF",
      "type": "GHG",
      "gwp": "4AR",
      "unit_numerator": "kg",
      "unit_denominator": "kWh",
      "CO2": 1000,
      "CH4": 100,
      "N2O": 100,
      "total_CO2e": 1000,
      "CO2b": 100,
      "data_quality": "",
      "year": 2019,
      "scale": "",
      "description": "",
      "source": ""
    }
  ]
})
headers = {
  'Content-Type': 'application/json'
}

response = requests.request("POST", url, headers=headers, data=payload)

print(response.text)

```

```php
<?php

$curl = curl_init();

curl_setopt_array($curl, array(
  CURLOPT_URL => 'https://dynm-corporate.herokuapp.com/community/transportation',
  CURLOPT_RETURNTRANSFER => true,
  CURLOPT_ENCODING => '',
  CURLOPT_MAXREDIRS => 10,
  CURLOPT_TIMEOUT => 0,
  CURLOPT_FOLLOWLOCATION => true,
  CURLOPT_HTTP_VERSION => CURL_HTTP_VERSION_1_1,
  CURLOPT_CUSTOMREQUEST => 'POST',
  CURLOPT_POSTFIELDS =>'{
    "gpc_ref": "II.1.1",
    "scope": "1",
    "fleet_type": "Municipal",
    "method": "Fuel sales approach",
    "description": "Stationary Emissions for Biodiesels fuel type",
    "activity": "Biodiesels",
    "category": "II.1 ON-ROAD TRANSPORTATION",
    "sub_category": "Emissions from fuel combustion on-road combustion ocurring in the city",
    "notation_key": "NO",
    "activity_amount": 1000,
    "activity_units": "kWh",
    "activity_multiplier_units": "kWh",
    "activity_multiplier": null,
    "oxidation_factor": 1,
    "gases": "CO2",
    "manual_emissions_data": false,
    "emission_factor": "Biodiesels EF",
    "CO2": null,
    "CH4": null,
    "total_CO2e": null,
    "CO2b": null,
    "N2O": null,
    "data_quality": "L",
    "methodology_description": "",
    "source": "",
    "data_quality_explanation": "",
    "custom_emission_factors": [
        {
            "activity": "Biodiesels",
            "reference": "Biodiesels EF",
            "type": "GHG",
            "gwp": "4AR",
            "unit_numerator": "kg",
            "unit_denominator": "kWh",
            "CO2": 1000,
            "CH4": 100,
            "N2O": 100,
            "total_CO2e": 1000,
            "CO2b": 100,
            "data_quality": "",
            "year": 2019,
            "scale": "",
            "description": "",
            "source": ""
        }
    ]
}',
  CURLOPT_HTTPHEADER => array(
    'Content-Type: application/json'
  ),
));

$response = curl_exec($curl);

curl_close($curl);
echo $response;


```

> RESPONSE : <code>200</code>

```json
{
  "CH4_tCO2e": 2500.0,
  "N20_tCO2e": 29799.999999999996,
  "TtCO2e": 1000.0,
  "tCO2b": 100.0,
  "tCO2e": 1000.0
}
```

Endpoint for recording activity and emissions data for Transportation sources.

`POST https://dynm-corporate.herokuapp.com/community/transportation`

<aside>Request params</aside>

| Param                     | Type    | Required | Description                                                                                                                                                                                             |
| ------------------------- | ------- | -------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| gpc_ref                   | string  | true     | The GPC reference string for this category e.g I.1.1 for the sub-category ‘Emissions from fuel combustion within the city boundary’ within Stationary Combustion’s category ‘I.1 RESIDENTIAL BUILDINGS’ |
| scope                     | string  | true     | The appropriate scope. One of 1, 2 or 3                                                                                                                                                                 |
| fleet_type                | string  | true     | The type of fleet used in calculation e.g Municipal                                                                                                                                                     |
| method                    | string  | true     | The calculation approach to be used in calculation e.g Fuel sales approach                                                                                                                              |
| description               | string  | nullable | General description of the row activity or calculation.                                                                                                                                                 |
| activity                  | string  | true     | The emission type or activity being reported on e.g Biodiesels                                                                                                                                          |
| category                  | string  | true     | The emission type or activity being reported on e.g Biodiesels                                                                                                                                          |
| sub_category              | string  | nullable | Appropriate sub-category under Inventory options with sub-categories e.g from the gpc_ref example above Emissions from fuel combustion within the city boundary                                         |
| sub_category_option       | string  | nullable | Appropriate sub(sub-category) under Inventory options with sub-categories e.g from the gpc_ref example above Residential 1.A.4.b                                                                        |
| notation_key              | string  | true     | Denote justifications for exclusion or partial accounting of GHG emission source categories. E.g NE for Not Estimated                                                                                   |
| activity_amount           | float   | true     | Amount of the units of the selected activity to report on. eg 100                                                                                                                                       |
| activity_units            | string  | true     | Measurement units for the activity data e.g kWh                                                                                                                                                         |
| activity_multiplier_units | string  | nullable | Units to be used if you wish to convert your data e.g kWh                                                                                                                                               |
| activity_multiplier       | float   | nullabke | An override value for converting activity data. If provided the conversion from activity_multiplier_units won’t be used rather this figure will be used. E.g 1.0                                        |
| oxidation_factor          | float   | nullable | Overrides default oxidation factor(1) e.g 1.0                                                                                                                                                           |
| gases                     | string  | nullable | Selection of gases in the reported emissions                                                                                                                                                            |
| manual_emissions_data     | boolean | true     | Indicates whether to use manually entered emission data or to calculate from an emission dataset. Defaults to false.                                                                                    |
| emission_factor           | string  | nullable | Name of the custom emission factor to be referenced. It is the reference field from one of the custom emission factors added. e.g Biodiesels_EF                                                         |
| CO2                       | float   | nullable | Manually entered C02 emissions                                                                                                                                                                          |
| CH4                       | float   | nullable | Manually entered CH4 emissions                                                                                                                                                                          |
| total_CO2e                | float   | nullable | Manually entered total_CO2e emissions                                                                                                                                                                   |
| CO2b                      | float   | nullable | Manually entered CO2b emissions                                                                                                                                                                         |
| N2O                       | float   | nullable | Manually entered N2O emissions                                                                                                                                                                          |
| data_quality              | string  | true     | Denotes quality of the submitted emissions data e.g L                                                                                                                                                   |
| methodology_description   | string  | nullable | Description of the methodology used for selecting a Notation Key                                                                                                                                        |
| source                    | string  | true     | The data source for the emissions or activity.                                                                                                                                                          |
| data_quality_explanation  | string  | true     | The explanation for choice of data quality level.                                                                                                                                                       |
| custom_emission_factors   | list    | true     | custom params for this particular endpoint                                                                                                                                                              |

# Community Waste

> REQUEST

```shell
curl --location --request POST 'https://dynm-corporate.herokuapp.com/community/waste' \
--header 'Content-Type: application/json' \
--data-raw '{
    "gpc_ref": "III.1.1",
    "scope": "1",
    "treatment_activity": "Landfill sites - Methane commitment",
    "waste_type": "All waste",
    "description": "Stationary Emissions for Biodiesels fuel type",
    "category": "III.1 SOLID WASTE DISPOSAL",
    "sub_category": "Emissions from solid waste generated in the city and disposed in landfills or open dumps within the city",
    "notation_key": "NO",
    "activity_amount": 1000,
    "activity_units": "kWh",
    "activity_multiplier_units": "kWh",
    "activity_multiplier": null,
    "oxidation_factor": 1,
    "gases": "CO2",
    "manual_emissions_data": false,
    "emission_factor": "Biodiesels EF",
    "CO2": null,
    "CH4": null,
    "total_CO2e": null,
    "CO2b": null,
    "N2O": null,
    "data_quality": "L",
    "methodology_description": "",
    "source": "",
    "data_quality_explanation": "",
    "custom_emission_factors": [
        {
            "activity": "Biodiesels",
            "reference": "Biodiesels EF",
            "type": "GHG",
            "gwp": "4AR",
            "unit_numerator": "kg",
            "unit_denominator": "kWh",
            "CO2": 1000,
            "CH4": 100,
            "N2O": 100,
            "total_CO2e": 1000,
            "CO2b": 100,
            "data_quality": "",
            "year": 2019,
            "scale": "",
            "description": "",
            "source": ""
        }
    ]
}'

```

```javascript
// const fetch = require("node-fetch");
import fetch from "node-fetch";
const data = {
  gpc_ref: "III.1.1",
  scope: "1",
  treatment_activity: "Landfill sites - Methane commitment",
  waste_type: "All waste",
  description: "Stationary Emissions for Biodiesels fuel type",
  category: "III.1 SOLID WASTE DISPOSAL",
  sub_category:
    "Emissions from solid waste generated in the city and disposed in landfills or open dumps within the city",
  notation_key: "NO",
  activity_amount: 1000,
  activity_units: "kWh",
  activity_multiplier_units: "kWh",
  activity_multiplier: null,
  oxidation_factor: 1,
  gases: "CO2",
  manual_emissions_data: false,
  emission_factor: "Biodiesels EF",
  CO2: null,
  CH4: null,
  total_CO2e: null,
  CO2b: null,
  N2O: null,
  data_quality: "L",
  methodology_description: "",
  source: "",
  data_quality_explanation: "",
  custom_emission_factors: [
    {
      activity: "Biodiesels",
      reference: "Biodiesels EF",
      type: "GHG",
      gwp: "4AR",
      unit_numerator: "kg",
      unit_denominator: "kWh",
      CO2: 1000,
      CH4: 100,
      N2O: 100,
      total_CO2e: 1000,
      CO2b: 100,
      data_quality: "",
      year: 2019,
      scale: "",
      description: "",
      source: "",
    },
  ],
};

fetch("https://dynm-corporate.herokuapp.com/community/waste", {
  method: "POST",
  headers: {
    "Content-Type": "application/json",
  },
  body: JSON.stringify(data),
})
  .then((response) => response.json())
  .then((data) => {
    console.log("Success:", data);
  })
  .catch((error) => {
    console.error("Error:", error);
  });
```

```python
import requests
import json

url = "https://dynm-corporate.herokuapp.com/community/waste"

payload = json.dumps({
  "gpc_ref": "III.1.1",
  "scope": "1",
  "treatment_activity": "Landfill sites - Methane commitment",
  "waste_type": "All waste",
  "description": "Stationary Emissions for Biodiesels fuel type",
  "category": "III.1 SOLID WASTE DISPOSAL",
  "sub_category": "Emissions from solid waste generated in the city and disposed in landfills or open dumps within the city",
  "notation_key": "NO",
  "activity_amount": 1000,
  "activity_units": "kWh",
  "activity_multiplier_units": "kWh",
  "activity_multiplier": None,
  "oxidation_factor": 1,
  "gases": "CO2",
  "manual_emissions_data": False,
  "emission_factor": "Biodiesels EF",
  "CO2": None,
  "CH4": None,
  "total_CO2e": None,
  "CO2b": None,
  "N2O": None,
  "data_quality": "L",
  "methodology_description": "",
  "source": "",
  "data_quality_explanation": "",
  "custom_emission_factors": [
    {
      "activity": "Biodiesels",
      "reference": "Biodiesels EF",
      "type": "GHG",
      "gwp": "4AR",
      "unit_numerator": "kg",
      "unit_denominator": "kWh",
      "CO2": 1000,
      "CH4": 100,
      "N2O": 100,
      "total_CO2e": 1000,
      "CO2b": 100,
      "data_quality": "",
      "year": 2019,
      "scale": "",
      "description": "",
      "source": ""
    }
  ]
})
headers = {
  'Content-Type': 'application/json'
}

response = requests.request("POST", url, headers=headers, data=payload)

print(response.text)

```

```php
<?php

$curl = curl_init();

curl_setopt_array($curl, array(
  CURLOPT_URL => 'https://dynm-corporate.herokuapp.com/community/waste',
  CURLOPT_RETURNTRANSFER => true,
  CURLOPT_ENCODING => '',
  CURLOPT_MAXREDIRS => 10,
  CURLOPT_TIMEOUT => 0,
  CURLOPT_FOLLOWLOCATION => true,
  CURLOPT_HTTP_VERSION => CURL_HTTP_VERSION_1_1,
  CURLOPT_CUSTOMREQUEST => 'POST',
  CURLOPT_POSTFIELDS =>'{
    "gpc_ref": "III.1.1",
    "scope": "1",
    "treatment_activity": "Landfill sites - Methane commitment",
    "waste_type": "All waste",
    "description": "Stationary Emissions for Biodiesels fuel type",
    "category": "III.1 SOLID WASTE DISPOSAL",
    "sub_category": "Emissions from solid waste generated in the city and disposed in landfills or open dumps within the city",
    "notation_key": "NO",
    "activity_amount": 1000,
    "activity_units": "kWh",
    "activity_multiplier_units": "kWh",
    "activity_multiplier": null,
    "oxidation_factor": 1,
    "gases": "CO2",
    "manual_emissions_data": false,
    "emission_factor": "Biodiesels EF",
    "CO2": null,
    "CH4": null,
    "total_CO2e": null,
    "CO2b": null,
    "N2O": null,
    "data_quality": "L",
    "methodology_description": "",
    "source": "",
    "data_quality_explanation": "",
    "custom_emission_factors": [
        {
            "activity": "Biodiesels",
            "reference": "Biodiesels EF",
            "type": "GHG",
            "gwp": "4AR",
            "unit_numerator": "kg",
            "unit_denominator": "kWh",
            "CO2": 1000,
            "CH4": 100,
            "N2O": 100,
            "total_CO2e": 1000,
            "CO2b": 100,
            "data_quality": "",
            "year": 2019,
            "scale": "",
            "description": "",
            "source": ""
        }
    ]
}',
  CURLOPT_HTTPHEADER => array(
    'Content-Type: application/json'
  ),
));

$response = curl_exec($curl);

curl_close($curl);
echo $response;


```

> RESPONSE : <code>200</code>

```json
{
  "CH4_tCO2e": 2500.0,
  "N20_tCO2e": 29799.999999999996,
  "TtCO2e": 1000.0,
  "tCO2b": 100.0,
  "tCO2e": 1000.0
}
```

Endpoint for recording activity and emissions data for Waste sources.

`POST https://dynm-corporate.herokuapp.com/community/waste`

<aside>Request params</aside>

| Param                     | Type    | Required | Description                                                                                                                                                                                             |
| ------------------------- | ------- | -------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| gpc_ref                   | string  | true     | The GPC reference string for this category e.g I.1.1 for the sub-category ‘Emissions from fuel combustion within the city boundary’ within Stationary Combustion’s category ‘I.1 RESIDENTIAL BUILDINGS’ |
| scope                     | string  | true     | The appropriate scope. One of 1, 2 or 3                                                                                                                                                                 |
| treatment_activity        | string  | true     | The waste treatment type being reported on e.g Landfill sites - Methane commitment                                                                                                                      |
| waste_type                | string  | true     | The type of waste used in calculation e.g Sludge                                                                                                                                                        |
| description               | string  | nullable | General description of the row activity or calculation.                                                                                                                                                 |
| category                  | string  | true     | The emission type or activity being reported on e.g Biodiesels                                                                                                                                          |
| sub_category              | string  | nullable | Appropriate sub-category under Inventory options with sub-categories e.g from the gpc_ref example above Emissions from fuel combustion within the city boundary                                         |
| sub_category_option       | string  | nullable | Appropriate sub(sub-category) under Inventory options with sub-categories e.g from the gpc_ref example above Residential 1.A.4.b                                                                        |
| notation_key              | string  | true     | Denote justifications for exclusion or partial accounting of GHG emission source categories. E.g NE for Not Estimated                                                                                   |
| activity_amount           | float   | true     | Amount of the units of the selected activity to report on. eg 100                                                                                                                                       |
| activity_units            | string  | true     | Measurement units for the activity data e.g kWh                                                                                                                                                         |
| activity_multiplier_units | string  | nullable | Units to be used if you wish to convert your data e.g kWh                                                                                                                                               |
| activity_multiplier       | float   | nullabke | An override value for converting activity data. If provided the conversion from activity_multiplier_units won’t be used rather this figure will be used. E.g 1.0                                        |
| oxidation_factor          | float   | nullable | Overrides default oxidation factor(1) e.g 1.0                                                                                                                                                           |
| gases                     | string  | nullable | Selection of gases in the reported emissions                                                                                                                                                            |
| manual_emissions_data     | boolean | true     | Indicates whether to use manually entered emission data or to calculate from an emission dataset. Defaults to false.                                                                                    |
| emission_factor           | string  | nullable | Name of the custom emission factor to be referenced. It is the reference field from one of the custom emission factors added. e.g Biodiesels_EF                                                         |
| CO2                       | float   | nullable | Manually entered C02 emissions                                                                                                                                                                          |
| CH4                       | float   | nullable | Manually entered CH4 emissions                                                                                                                                                                          |
| total_CO2e                | float   | nullable | Manually entered total_CO2e emissions                                                                                                                                                                   |
| CO2b                      | float   | nullable | Manually entered CO2b emissions                                                                                                                                                                         |
| N2O                       | float   | nullable | Manually entered N2O emissions                                                                                                                                                                          |
| data_quality              | string  | true     | Denotes quality of the submitted emissions data e.g L                                                                                                                                                   |
| methodology_description   | string  | nullable | Description of the methodology used for selecting a Notation Key                                                                                                                                        |
| source                    | string  | true     | The data source for the emissions or activity.                                                                                                                                                          |
| data_quality_explanation  | string  | true     | The explanation for choice of data quality level.                                                                                                                                                       |
| custom_emission_factors   | list    | true     | custom params for this particular endpoint                                                                                                                                                              |

# Community IPPU

> REQUEST

```shell
curl --location --request POST 'https://dynm-corporate.herokuapp.com/community/ippu' \
--header 'Content-Type: application/json' \
--data-raw '{
    "gpc_ref": "IV.1",
    "scope": "1",
    "industry": "Mineral",
    "industrial_process": "Cement production (2.A.1)",
    "description": "Stationary Emissions for Biodiesels fuel type",
    "category": "IV.1 INDUSTRIAL PROCESS",
    "sub_category": "Emissions from fuel combustion on-road combustion ocurring in the city",
    "notation_key": "NO",
    "activity_amount": 1000,
    "activity_units": "kWh",
    "activity_multiplier_units": "kWh",
    "activity_multiplier": null,
    "oxidation_factor": 1,
    "gases": "CO2",
    "manual_emissions_data": false,
    "emission_factor": "Biodiesels EF",
    "CO2": null,
    "CH4": null,
    "total_CO2e": null,
    "CO2b": null,
    "N2O": null,
    "data_quality": "L",
    "methodology_description": "",
    "source": "",
    "data_quality_explanation": "",
    "custom_emission_factors": [
        {
            "activity": "Biodiesels",
            "reference": "Biodiesels EF",
            "type": "GHG",
            "gwp": "4AR",
            "unit_numerator": "kg",
            "unit_denominator": "kWh",
            "CO2": 1000,
            "CH4": 100,
            "N2O": 100,
            "total_CO2e": 1000,
            "CO2b": 100,
            "data_quality": "",
            "year": 2019,
            "scale": "",
            "description": "",
            "source": ""
        }
    ]
}'

```

```javascript
// const fetch = require("node-fetch");
import fetch from "node-fetch";
const data = {
  gpc_ref: "IV.1",
  scope: "1",
  industry: "Mineral",
  industrial_process: "Cement production (2.A.1)",
  description: "Stationary Emissions for Biodiesels fuel type",
  category: "IV.1 INDUSTRIAL PROCESS",
  sub_category:
    "Emissions from fuel combustion on-road combustion ocurring in the city",
  notation_key: "NO",
  activity_amount: 1000,
  activity_units: "kWh",
  activity_multiplier_units: "kWh",
  activity_multiplier: null,
  oxidation_factor: 1,
  gases: "CO2",
  manual_emissions_data: false,
  emission_factor: "Biodiesels EF",
  CO2: null,
  CH4: null,
  total_CO2e: null,
  CO2b: null,
  N2O: null,
  data_quality: "L",
  methodology_description: "",
  source: "",
  data_quality_explanation: "",
  custom_emission_factors: [
    {
      activity: "Biodiesels",
      reference: "Biodiesels EF",
      type: "GHG",
      gwp: "4AR",
      unit_numerator: "kg",
      unit_denominator: "kWh",
      CO2: 1000,
      CH4: 100,
      N2O: 100,
      total_CO2e: 1000,
      CO2b: 100,
      data_quality: "",
      year: 2019,
      scale: "",
      description: "",
      source: "",
    },
  ],
};

fetch("https://dynm-corporate.herokuapp.com/community/ippu", {
  method: "POST",
  headers: {
    "Content-Type": "application/json",
  },
  body: JSON.stringify(data),
})
  .then((response) => response.json())
  .then((data) => {
    console.log("Success:", data);
  })
  .catch((error) => {
    console.error("Error:", error);
  });
```

```python
import requests
import json

url = "https://dynm-corporate.herokuapp.com/community/ippu"

payload = json.dumps({
  "gpc_ref": "IV.1",
  "scope": "1",
  "industry": "Mineral",
  "industrial_process": "Cement production (2.A.1)",
  "description": "Stationary Emissions for Biodiesels fuel type",
  "category": "IV.1 INDUSTRIAL PROCESS",
  "sub_category": "Emissions from fuel combustion on-road combustion ocurring in the city",
  "notation_key": "NO",
  "activity_amount": 1000,
  "activity_units": "kWh",
  "activity_multiplier_units": "kWh",
  "activity_multiplier": None,
  "oxidation_factor": 1,
  "gases": "CO2",
  "manual_emissions_data": False,
  "emission_factor": "Biodiesels EF",
  "CO2": None,
  "CH4": None,
  "total_CO2e": None,
  "CO2b": None,
  "N2O": None,
  "data_quality": "L",
  "methodology_description": "",
  "source": "",
  "data_quality_explanation": "",
  "custom_emission_factors": [
    {
      "activity": "Biodiesels",
      "reference": "Biodiesels EF",
      "type": "GHG",
      "gwp": "4AR",
      "unit_numerator": "kg",
      "unit_denominator": "kWh",
      "CO2": 1000,
      "CH4": 100,
      "N2O": 100,
      "total_CO2e": 1000,
      "CO2b": 100,
      "data_quality": "",
      "year": 2019,
      "scale": "",
      "description": "",
      "source": ""
    }
  ]
})
headers = {
  'Content-Type': 'application/json'
}

response = requests.request("POST", url, headers=headers, data=payload)

print(response.text)

```

```php
<?php

$curl = curl_init();

curl_setopt_array($curl, array(
  CURLOPT_URL => 'https://dynm-corporate.herokuapp.com/community/ippu',
  CURLOPT_RETURNTRANSFER => true,
  CURLOPT_ENCODING => '',
  CURLOPT_MAXREDIRS => 10,
  CURLOPT_TIMEOUT => 0,
  CURLOPT_FOLLOWLOCATION => true,
  CURLOPT_HTTP_VERSION => CURL_HTTP_VERSION_1_1,
  CURLOPT_CUSTOMREQUEST => 'POST',
  CURLOPT_POSTFIELDS =>'{
    "gpc_ref": "IV.1",
    "scope": "1",
    "industry": "Mineral",
    "industrial_process": "Cement production (2.A.1)",
    "description": "Stationary Emissions for Biodiesels fuel type",
    "category": "IV.1 INDUSTRIAL PROCESS",
    "sub_category": "Emissions from fuel combustion on-road combustion ocurring in the city",
    "notation_key": "NO",
    "activity_amount": 1000,
    "activity_units": "kWh",
    "activity_multiplier_units": "kWh",
    "activity_multiplier": null,
    "oxidation_factor": 1,
    "gases": "CO2",
    "manual_emissions_data": false,
    "emission_factor": "Biodiesels EF",
    "CO2": null,
    "CH4": null,
    "total_CO2e": null,
    "CO2b": null,
    "N2O": null,
    "data_quality": "L",
    "methodology_description": "",
    "source": "",
    "data_quality_explanation": "",
    "custom_emission_factors": [
        {
            "activity": "Biodiesels",
            "reference": "Biodiesels EF",
            "type": "GHG",
            "gwp": "4AR",
            "unit_numerator": "kg",
            "unit_denominator": "kWh",
            "CO2": 1000,
            "CH4": 100,
            "N2O": 100,
            "total_CO2e": 1000,
            "CO2b": 100,
            "data_quality": "",
            "year": 2019,
            "scale": "",
            "description": "",
            "source": ""
        }
    ]
}',
  CURLOPT_HTTPHEADER => array(
    'Content-Type: application/json'
  ),
));

$response = curl_exec($curl);

curl_close($curl);
echo $response;


```

> RESPONSE : <code>200</code>

```json
{
  "CH4_tCO2e": 2500.0,
  "N20_tCO2e": 29799.999999999996,
  "TtCO2e": 1000.0,
  "tCO2b": 100.0,
  "tCO2e": 1000.0
}
```

Endpoint for recording activity and emissions data for IPPU sources.

`POST https://dynm-corporate.herokuapp.com/community/ippu`

<aside>Request params</aside>

| Param                     | Type    | Required | Description                                                                                                                                                                                             |
| ------------------------- | ------- | -------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| gpc_ref                   | string  | true     | The GPC reference string for this category e.g I.1.1 for the sub-category ‘Emissions from fuel combustion within the city boundary’ within Stationary Combustion’s category ‘I.1 RESIDENTIAL BUILDINGS’ |
| scope                     | string  | true     | The appropriate scope. One of 1, 2 or 3                                                                                                                                                                 |
| industry                  | string  | true     | The industry being reported e.g Mineral                                                                                                                                                                 |
| industrial_process        | string  | true     | The industrial process being reported e.g Cement production (2.A.1)                                                                                                                                     |
| description               | string  | nullable | General description of the row activity or calculation.                                                                                                                                                 |
| category                  | string  | true     | The emission type or activity being reported on e.g Biodiesels                                                                                                                                          |
| sub_category              | string  | nullable | Appropriate sub-category under Inventory options with sub-categories e.g from the gpc_ref example above Emissions from fuel combustion within the city boundary                                         |
| sub_category_option       | string  | nullable | Appropriate sub(sub-category) under Inventory options with sub-categories e.g from the gpc_ref example above Residential 1.A.4.b                                                                        |
| notation_key              | string  | true     | Denote justifications for exclusion or partial accounting of GHG emission source categories. E.g NE for Not Estimated                                                                                   |
| activity_amount           | float   | true     | Amount of the units of the selected activity to report on. eg 100                                                                                                                                       |
| activity_units            | string  | true     | Measurement units for the activity data e.g kWh                                                                                                                                                         |
| activity_multiplier_units | string  | nullable | Units to be used if you wish to convert your data e.g kWh                                                                                                                                               |
| activity_multiplier       | float   | nullabke | An override value for converting activity data. If provided the conversion from activity_multiplier_units won’t be used rather this figure will be used. E.g 1.0                                        |
| oxidation_factor          | float   | nullable | Overrides default oxidation factor(1) e.g 1.0                                                                                                                                                           |
| gases                     | string  | nullable | Selection of gases in the reported emissions                                                                                                                                                            |
| manual_emissions_data     | boolean | true     | Indicates whether to use manually entered emission data or to calculate from an emission dataset. Defaults to false.                                                                                    |
| emission_factor           | string  | nullable | Name of the custom emission factor to be referenced. It is the reference field from one of the custom emission factors added. e.g Biodiesels_EF                                                         |
| CO2                       | float   | nullable | Manually entered C02 emissions                                                                                                                                                                          |
| CH4                       | float   | nullable | Manually entered CH4 emissions                                                                                                                                                                          |
| total_CO2e                | float   | nullable | Manually entered total_CO2e emissions                                                                                                                                                                   |
| CO2b                      | float   | nullable | Manually entered CO2b emissions                                                                                                                                                                         |
| N2O                       | float   | nullable | Manually entered N2O emissions                                                                                                                                                                          |
| data_quality              | string  | true     | Denotes quality of the submitted emissions data e.g L                                                                                                                                                   |
| methodology_description   | string  | nullable | Description of the methodology used for selecting a Notation Key                                                                                                                                        |
| source                    | string  | true     | The data source for the emissions or activity.                                                                                                                                                          |
| data_quality_explanation  | string  | true     | The explanation for choice of data quality level.                                                                                                                                                       |
| custom_emission_factors   | list    | true     | custom params for this particular endpoint                                                                                                                                                              |

# Community AFOLU

> REQUEST

```shell
curl --location --request POST 'https://dynm-corporate.herokuapp.com/community/afolu' \
--header 'Content-Type: application/json' \
--data-raw '{
    "gpc_ref": "V.1",
    "scope": "1",
    "description": "Stationary Emissions for Biodiesels fuel type",
    "activity": "All livestock (3.A)",
    "category": "V.1 LIVESTOCK",
    "sub_category": "Emissions from livestock",
    "notation_key": "NO",
    "activity_amount": 1000,
    "activity_units": "kWh",
    "activity_multiplier_units": "kWh",
    "activity_multiplier": null,
    "oxidation_factor": 1,
    "gases": "CO2",
    "manual_emissions_data": false,
    "emission_factor": "Biodiesels EF",
    "CO2": null,
    "CH4": null,
    "total_CO2e": null,
    "CO2b": null,
    "N2O": null,
    "data_quality": "L",
    "methodology_description": "",
    "source": "",
    "data_quality_explanation": "",
    "custom_emission_factors": [
        {
            "activity": "Biodiesels",
            "reference": "Biodiesels EF",
            "type": "GHG",
            "gwp": "4AR",
            "unit_numerator": "kg",
            "unit_denominator": "kWh",
            "CO2": 1000,
            "CH4": 100,
            "N2O": 100,
            "total_CO2e": 1000,
            "CO2b": 100,
            "data_quality": "",
            "year": 2019,
            "scale": "",
            "description": "",
            "source": ""
        }
    ]
}'

```

```javascript
// const fetch = require("node-fetch");
import fetch from "node-fetch";
const data = {
  gpc_ref: "V.1",
  scope: "1",
  description: "Stationary Emissions for Biodiesels fuel type",
  activity: "All livestock (3.A)",
  category: "V.1 LIVESTOCK",
  sub_category: "Emissions from livestock",
  notation_key: "NO",
  activity_amount: 1000,
  activity_units: "kWh",
  activity_multiplier_units: "kWh",
  activity_multiplier: null,
  oxidation_factor: 1,
  gases: "CO2",
  manual_emissions_data: false,
  emission_factor: "Biodiesels EF",
  CO2: null,
  CH4: null,
  total_CO2e: null,
  CO2b: null,
  N2O: null,
  data_quality: "L",
  methodology_description: "",
  source: "",
  data_quality_explanation: "",
  custom_emission_factors: [
    {
      activity: "Biodiesels",
      reference: "Biodiesels EF",
      type: "GHG",
      gwp: "4AR",
      unit_numerator: "kg",
      unit_denominator: "kWh",
      CO2: 1000,
      CH4: 100,
      N2O: 100,
      total_CO2e: 1000,
      CO2b: 100,
      data_quality: "",
      year: 2019,
      scale: "",
      description: "",
      source: "",
    },
  ],
};

fetch("https://dynm-corporate.herokuapp.com/community/afolu", {
  method: "POST",
  headers: {
    "Content-Type": "application/json",
  },
  body: JSON.stringify(data),
})
  .then((response) => response.json())
  .then((data) => {
    console.log("Success:", data);
  })
  .catch((error) => {
    console.error("Error:", error);
  });
```

```python
import requests
import json

url = "https://dynm-corporate.herokuapp.com/community/afolu"

payload = json.dumps({
  "gpc_ref": "V.1",
  "scope": "1",
  "description": "Stationary Emissions for Biodiesels fuel type",
  "activity": "All livestock (3.A)",
  "category": "V.1 LIVESTOCK",
  "sub_category": "Emissions from livestock",
  "notation_key": "NO",
  "activity_amount": 1000,
  "activity_units": "kWh",
  "activity_multiplier_units": "kWh",
  "activity_multiplier": None,
  "oxidation_factor": 1,
  "gases": "CO2",
  "manual_emissions_data": False,
  "emission_factor": "Biodiesels EF",
  "CO2": None,
  "CH4": None,
  "total_CO2e": None,
  "CO2b": None,
  "N2O": None,
  "data_quality": "L",
  "methodology_description": "",
  "source": "",
  "data_quality_explanation": "",
  "custom_emission_factors": [
    {
      "activity": "Biodiesels",
      "reference": "Biodiesels EF",
      "type": "GHG",
      "gwp": "4AR",
      "unit_numerator": "kg",
      "unit_denominator": "kWh",
      "CO2": 1000,
      "CH4": 100,
      "N2O": 100,
      "total_CO2e": 1000,
      "CO2b": 100,
      "data_quality": "",
      "year": 2019,
      "scale": "",
      "description": "",
      "source": ""
    }
  ]
})
headers = {
  'Content-Type': 'application/json'
}

response = requests.request("POST", url, headers=headers, data=payload)

print(response.text)

```

```php
<?php

$curl = curl_init();

curl_setopt_array($curl, array(
  CURLOPT_URL => 'https://dynm-corporate.herokuapp.com/community/afolu',
  CURLOPT_RETURNTRANSFER => true,
  CURLOPT_ENCODING => '',
  CURLOPT_MAXREDIRS => 10,
  CURLOPT_TIMEOUT => 0,
  CURLOPT_FOLLOWLOCATION => true,
  CURLOPT_HTTP_VERSION => CURL_HTTP_VERSION_1_1,
  CURLOPT_CUSTOMREQUEST => 'POST',
  CURLOPT_POSTFIELDS =>'{
    "gpc_ref": "V.1",
    "scope": "1",
    "description": "Stationary Emissions for Biodiesels fuel type",
    "activity": "All livestock (3.A)",
    "category": "V.1 LIVESTOCK",
    "sub_category": "Emissions from livestock",
    "notation_key": "NO",
    "activity_amount": 1000,
    "activity_units": "kWh",
    "activity_multiplier_units": "kWh",
    "activity_multiplier": null,
    "oxidation_factor": 1,
    "gases": "CO2",
    "manual_emissions_data": false,
    "emission_factor": "Biodiesels EF",
    "CO2": null,
    "CH4": null,
    "total_CO2e": null,
    "CO2b": null,
    "N2O": null,
    "data_quality": "L",
    "methodology_description": "",
    "source": "",
    "data_quality_explanation": "",
    "custom_emission_factors": [
        {
            "activity": "Biodiesels",
            "reference": "Biodiesels EF",
            "type": "GHG",
            "gwp": "4AR",
            "unit_numerator": "kg",
            "unit_denominator": "kWh",
            "CO2": 1000,
            "CH4": 100,
            "N2O": 100,
            "total_CO2e": 1000,
            "CO2b": 100,
            "data_quality": "",
            "year": 2019,
            "scale": "",
            "description": "",
            "source": ""
        }
    ]
}',
  CURLOPT_HTTPHEADER => array(
    'Content-Type: application/json'
  ),
));

$response = curl_exec($curl);

curl_close($curl);
echo $response;


```

> RESPONSE : <code>200</code>

```json
{
  "CH4_tCO2e": 2500.0,
  "N20_tCO2e": 29799.999999999996,
  "TtCO2e": 1000.0,
  "tCO2b": 100.0,
  "tCO2e": 1000.0
}
```

Endpoint for recording activity and emissions data for AFOLU sources.

`POST https://dynm-corporate.herokuapp.com/community/afolu`

<aside>Request params</aside>

| Param                     | Type    | Required | Description                                                                                                                                                                                             |
| ------------------------- | ------- | -------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| gpc_ref                   | string  | true     | The GPC reference string for this category e.g I.1.1 for the sub-category ‘Emissions from fuel combustion within the city boundary’ within Stationary Combustion’s category ‘I.1 RESIDENTIAL BUILDINGS’ |
| scope                     | string  | true     | The appropriate scope. One of 1, 2 or 3                                                                                                                                                                 |
| description               | string  | nullable | General description of the row activity or calculation.                                                                                                                                                 |
| activity                  | string  | true     | The agricultural emission type or activity being reported on e.g Forest land                                                                                                                            |
| category                  | string  | true     | The emission type or activity being reported on e.g Biodiesels                                                                                                                                          |
| sub_category              | string  | nullable | Appropriate sub-category under Inventory options with sub-categories e.g from the gpc_ref example above Emissions from fuel combustion within the city boundary                                         |
| sub_category_option       | string  | nullable | Appropriate sub(sub-category) under Inventory options with sub-categories e.g from the gpc_ref example above Residential 1.A.4.b                                                                        |
| notation_key              | string  | true     | Denote justifications for exclusion or partial accounting of GHG emission source categories. E.g NE for Not Estimated                                                                                   |
| activity_amount           | float   | true     | Amount of the units of the selected activity to report on. eg 100                                                                                                                                       |
| activity_units            | string  | true     | Measurement units for the activity data e.g kWh                                                                                                                                                         |
| activity_multiplier_units | string  | nullable | Units to be used if you wish to convert your data e.g kWh                                                                                                                                               |
| activity_multiplier       | float   | nullabke | An override value for converting activity data. If provided the conversion from activity_multiplier_units won’t be used rather this figure will be used. E.g 1.0                                        |
| oxidation_factor          | float   | nullable | Overrides default oxidation factor(1) e.g 1.0                                                                                                                                                           |
| gases                     | string  | nullable | Selection of gases in the reported emissions                                                                                                                                                            |
| manual_emissions_data     | boolean | true     | Indicates whether to use manually entered emission data or to calculate from an emission dataset. Defaults to false.                                                                                    |
| emission_factor           | string  | nullable | Name of the custom emission factor to be referenced. It is the reference field from one of the custom emission factors added. e.g Biodiesels_EF                                                         |
| CO2                       | float   | nullable | Manually entered C02 emissions                                                                                                                                                                          |
| CH4                       | float   | nullable | Manually entered CH4 emissions                                                                                                                                                                          |
| total_CO2e                | float   | nullable | Manually entered total_CO2e emissions                                                                                                                                                                   |
| CO2b                      | float   | nullable | Manually entered CO2b emissions                                                                                                                                                                         |
| N2O                       | float   | nullable | Manually entered N2O emissions                                                                                                                                                                          |
| data_quality              | string  | true     | Denotes quality of the submitted emissions data e.g L                                                                                                                                                   |
| methodology_description   | string  | nullable | Description of the methodology used for selecting a Notation Key                                                                                                                                        |
| source                    | string  | true     | The data source for the emissions or activity.                                                                                                                                                          |
| data_quality_explanation  | string  | true     | The explanation for choice of data quality level.                                                                                                                                                       |
| custom_emission_factors   | list    | true     | custom params for this particular endpoint                                                                                                                                                              |

# Community Other Scope

> REQUEST

```shell
curl --location --request POST 'https://dynm-corporate.herokuapp.com/community/other' \
--header 'Content-Type: application/json' \
--data-raw '{
    "gpc_ref": "VI.1",
    "scope": "3",
    "description": "Stationary Emissions for Biodiesels fuel type",
    "activity": "Food",
    "category": "VI.1 OTHER SCOPE 3",
    "sub_category": "Emissions from fuel combustion on-road combustion ocurring in the city",
    "notation_key": "NO",
    "activity_amount": 1000,
    "activity_units": "kWh",
    "activity_multiplier_units": "kWh",
    "activity_multiplier": null,
    "oxidation_factor": 1,
    "gases": "CO2",
    "manual_emissions_data": false,
    "emission_factor": "Biodiesels EF",
    "CO2": null,
    "CH4": null,
    "total_CO2e": null,
    "CO2b": null,
    "N2O": null,
    "data_quality": "L",
    "methodology_description": "",
    "source": "",
    "data_quality_explanation": "",
    "custom_emission_factors": [
        {
            "activity": "Biodiesels",
            "reference": "Biodiesels EF",
            "type": "GHG",
            "gwp": "4AR",
            "unit_numerator": "kg",
            "unit_denominator": "kWh",
            "CO2": 1000,
            "CH4": 100,
            "N2O": 100,
            "total_CO2e": 1000,
            "CO2b": 100,
            "data_quality": "",
            "year": 2019,
            "scale": "",
            "description": "",
            "source": ""
        }
    ]
}'
```

```javascript
// const fetch = require("node-fetch");
import fetch from "node-fetch";
const data = {
  gpc_ref: "VI.1",
  scope: "3",
  description: "Stationary Emissions for Biodiesels fuel type",
  activity: "Food",
  category: "VI.1 OTHER SCOPE 3",
  sub_category:
    "Emissions from fuel combustion on-road combustion ocurring in the city",
  notation_key: "NO",
  activity_amount: 1000,
  activity_units: "kWh",
  activity_multiplier_units: "kWh",
  activity_multiplier: null,
  oxidation_factor: 1,
  gases: "CO2",
  manual_emissions_data: false,
  emission_factor: "Biodiesels EF",
  CO2: null,
  CH4: null,
  total_CO2e: null,
  CO2b: null,
  N2O: null,
  data_quality: "L",
  methodology_description: "",
  source: "",
  data_quality_explanation: "",
  custom_emission_factors: [
    {
      activity: "Biodiesels",
      reference: "Biodiesels EF",
      type: "GHG",
      gwp: "4AR",
      unit_numerator: "kg",
      unit_denominator: "kWh",
      CO2: 1000,
      CH4: 100,
      N2O: 100,
      total_CO2e: 1000,
      CO2b: 100,
      data_quality: "",
      year: 2019,
      scale: "",
      description: "",
      source: "",
    },
  ],
};

fetch("https://dynm-corporate.herokuapp.com/community/other", {
  method: "POST",
  headers: {
    "Content-Type": "application/json",
  },
  body: JSON.stringify(data),
})
  .then((response) => response.json())
  .then((data) => {
    console.log("Success:", data);
  })
  .catch((error) => {
    console.error("Error:", error);
  });
```

```python
import requests
import json

url = "https://dynm-corporate.herokuapp.com/community/other"

payload = json.dumps({
  "gpc_ref": "VI.1",
  "scope": "3",
  "description": "Stationary Emissions for Biodiesels fuel type",
  "activity": "Food",
  "category": "VI.1 OTHER SCOPE 3",
  "sub_category": "Emissions from fuel combustion on-road combustion ocurring in the city",
  "notation_key": "NO",
  "activity_amount": 1000,
  "activity_units": "kWh",
  "activity_multiplier_units": "kWh",
  "activity_multiplier": None,
  "oxidation_factor": 1,
  "gases": "CO2",
  "manual_emissions_data": False,
  "emission_factor": "Biodiesels EF",
  "CO2": None,
  "CH4": None,
  "total_CO2e": None,
  "CO2b": None,
  "N2O": None,
  "data_quality": "L",
  "methodology_description": "",
  "source": "",
  "data_quality_explanation": "",
  "custom_emission_factors": [
    {
      "activity": "Biodiesels",
      "reference": "Biodiesels EF",
      "type": "GHG",
      "gwp": "4AR",
      "unit_numerator": "kg",
      "unit_denominator": "kWh",
      "CO2": 1000,
      "CH4": 100,
      "N2O": 100,
      "total_CO2e": 1000,
      "CO2b": 100,
      "data_quality": "",
      "year": 2019,
      "scale": "",
      "description": "",
      "source": ""
    }
  ]
})
headers = {
  'Content-Type': 'application/json'
}

response = requests.request("POST", url, headers=headers, data=payload)

print(response.text)

```

```php
<?php

$curl = curl_init();

curl_setopt_array($curl, array(
  CURLOPT_URL => 'https://dynm-corporate.herokuapp.com/community/other',
  CURLOPT_RETURNTRANSFER => true,
  CURLOPT_ENCODING => '',
  CURLOPT_MAXREDIRS => 10,
  CURLOPT_TIMEOUT => 0,
  CURLOPT_FOLLOWLOCATION => true,
  CURLOPT_HTTP_VERSION => CURL_HTTP_VERSION_1_1,
  CURLOPT_CUSTOMREQUEST => 'POST',
  CURLOPT_POSTFIELDS =>'{
    "gpc_ref": "VI.1",
    "scope": "3",
    "description": "Stationary Emissions for Biodiesels fuel type",
    "activity": "Food",
    "category": "VI.1 OTHER SCOPE 3",
    "sub_category": "Emissions from fuel combustion on-road combustion ocurring in the city",
    "notation_key": "NO",
    "activity_amount": 1000,
    "activity_units": "kWh",
    "activity_multiplier_units": "kWh",
    "activity_multiplier": null,
    "oxidation_factor": 1,
    "gases": "CO2",
    "manual_emissions_data": false,
    "emission_factor": "Biodiesels EF",
    "CO2": null,
    "CH4": null,
    "total_CO2e": null,
    "CO2b": null,
    "N2O": null,
    "data_quality": "L",
    "methodology_description": "",
    "source": "",
    "data_quality_explanation": "",
    "custom_emission_factors": [
        {
            "activity": "Biodiesels",
            "reference": "Biodiesels EF",
            "type": "GHG",
            "gwp": "4AR",
            "unit_numerator": "kg",
            "unit_denominator": "kWh",
            "CO2": 1000,
            "CH4": 100,
            "N2O": 100,
            "total_CO2e": 1000,
            "CO2b": 100,
            "data_quality": "",
            "year": 2019,
            "scale": "",
            "description": "",
            "source": ""
        }
    ]
}',
  CURLOPT_HTTPHEADER => array(
    'Content-Type: application/json'
  ),
));

$response = curl_exec($curl);

curl_close($curl);
echo $response;


```

> RESPONSE : <code>200</code>

```json
{
  "CH4_tCO2e": 2500.0,
  "N20_tCO2e": 29799.999999999996,
  "TtCO2e": 1000.0,
  "tCO2b": 100.0,
  "tCO2e": 1000.0
}
```

Endpoint for recording activity and emissions data for Other Scope 3 sources.

`POST https://dynm-corporate.herokuapp.com/community/other`

<aside>Request params</aside>

| Param                     | Type    | Required | Description                                                                                                                                                                                             |
| ------------------------- | ------- | -------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| gpc_ref                   | string  | true     | The GPC reference string for this category e.g I.1.1 for the sub-category ‘Emissions from fuel combustion within the city boundary’ within Stationary Combustion’s category ‘I.1 RESIDENTIAL BUILDINGS’ |
| scope                     | string  | true     | The appropriate scope. One of 1, 2 or 3                                                                                                                                                                 |
| description               | string  | nullable | General description of the row activity or calculation.                                                                                                                                                 |
| activity                  | string  | true     | The emission type or activity being reported on e.g Food                                                                                                                                                |
| category                  | string  | true     | The emission type or activity being reported on e.g Biodiesels                                                                                                                                          |
| sub_category              | string  | nullable | Appropriate sub-category under Inventory options with sub-categories e.g from the gpc_ref example above Emissions from fuel combustion within the city boundary                                         |
| notation_key              | string  | true     | Denote justifications for exclusion or partial accounting of GHG emission source categories. E.g NE for Not Estimated                                                                                   |
| activity_amount           | float   | true     | Amount of the units of the selected activity to report on. eg 100                                                                                                                                       |
| activity_units            | string  | true     | Measurement units for the activity data e.g kWh                                                                                                                                                         |
| activity_multiplier_units | string  | nullable | Units to be used if you wish to convert your data e.g kWh                                                                                                                                               |
| activity_multiplier       | float   | nullabke | An override value for converting activity data. If provided the conversion from activity_multiplier_units won’t be used rather this figure will be used. E.g 1.0                                        |
| oxidation_factor          | float   | nullable | Overrides default oxidation factor(1) e.g 1.0                                                                                                                                                           |
| gases                     | string  | nullable | Selection of gases in the reported emissions                                                                                                                                                            |
| manual_emissions_data     | boolean | true     | Indicates whether to use manually entered emission data or to calculate from an emission dataset. Defaults to false.                                                                                    |
| emission_factor           | string  | nullable | Name of the custom emission factor to be referenced. It is the reference field from one of the custom emission factors added. e.g Biodiesels_EF                                                         |
| CO2                       | float   | nullable | Manually entered C02 emissions                                                                                                                                                                          |
| CH4                       | float   | nullable | Manually entered CH4 emissions                                                                                                                                                                          |
| total_CO2e                | float   | nullable | Manually entered total_CO2e emissions                                                                                                                                                                   |
| CO2b                      | float   | nullable | Manually entered CO2b emissions                                                                                                                                                                         |
| N2O                       | float   | nullable | Manually entered N2O emissions                                                                                                                                                                          |
| data_quality              | string  | true     | Denotes quality of the submitted emissions data e.g L                                                                                                                                                   |
| methodology_description   | string  | nullable | Description of the methodology used for selecting a Notation Key                                                                                                                                        |
| source                    | string  | true     | The data source for the emissions or activity.                                                                                                                                                          |
| data_quality_explanation  | string  | true     | The explanation for choice of data quality level.                                                                                                                                                       |
| custom_emission_factors   | list    | true     | custom params for this particular endpoint                                                                                                                                                              |
