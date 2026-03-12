## List all licences

> <span style="font-family:Consolas, Menlo, Monaco, \"Lucida Console\", \"Liberation Mono\", \"DejaVu Sans Mono\", \"Bitstream Vera Sans Mono\", \"Courier New\", monospace, serif"><span style="color:#a4cdfe">GET</span> /licences</span>

```shell
$ curl 'https://your_council.metastreet.co.uk/api/v1.1/licences?postcode=A12BC&licenceTypeId=3' \
-H 'x-auth-api-token: 3b07c593c309ebf41330cd6f6867610eb18abe43dcf1d'
```

> EXAMPLE RESPONSE

```json
{
  "object": "licence",
  "url": "/api/v1.1/licences",
  "pageSize": 100,
  "currentPage": 1,
  "totalPages": 5,
  "totalCount": 401,
  "data": [
    {
      "referenceNumber": "YCO-583484913397",
      "address": {
        "addressLine1": "4 Dasher Place",
        "addressLine2": "Dasher Street",
        "addressLine3": "Dasher Estate",
        "addressLine4": "Dasher",
        "city": "London",
        "country": "United Kingdom",
        "postcode": "A1 2BC",
        "uprn": "12345678910",
        "usrn": "1234567",
        "latitude": "1.230045",
        "longitude": "-5.430021",
        "ward": "Dasher Ward"
      },
      "licencePhase": "Application",
      "licenceType": {
        "id": 3,
        "name": "Selective licence"
      },
      "licenceStatus": {
        "id": 12,
        "name": "Checks in progress"
      },
      "assignee": {
        "id": 7,
        "name": "Finn Wood"
      },
      "assignedTeam": {
        "id": 1,
        "name": "Enforcement Team",
        "category": "Enforcement"
      },
      "dateSubmitted": "2021-11-26T09:32:08+00:00",
      "datePaid": "2021-11-26T09:32:08+00:00",
      "propertyRooms": {
        "bathrooms": [
          {
            "location": "First floor rear",
            "exclusivity": "Shared",
            "washHandBasins": 1,
            "toilets": 1,
            "bathsAndShowers": 2
          }
        ],
        "bedrooms": [
          {
            "location": "First floor front",
            "size": 25.0,
            "exclusivity": "Exclusive",
            "bathroomFacilities": "No",
            "washBasins": 0,
            "toilets": 0,
            "bathShower": 0,
            "kitchenFacilities": "No",
            "ovens": 0,
            "hobs": 0,
            "sinks": 0,
            "fridges": 0,
            "freezers": 0
          }
        ],
        "communalRooms": [
          {
            "location": "Ground floor north side",
            "size": 45.0,
            "exclusivity": "Shared",
            "smokeAlarm": "Yes",
            "bestDescription": "Living room",
            "washHandBasins": 0
          }
        ],
        "kitchens": [
          {
            "location": "Ground floor rear",
            "size": 15.45,
            "exclusivity": "Shared",
            "smokeAlarm": "Yes",
            "ovens": 1,
            "hobs": 1,
            "sinks": 1,
            "fridges": 1,
            "freezers": 1
          }
        ]
        ...
      },
      "eligibilityInformation": {
        "unspentConvictions": "No",
        "unlawfulDiscrimination": "No",
        "judgementMadeAgainstYou": "No",
        "experienceOfManagingRentedProperty": "No",
        "licenceHolderBelongToLandlords": "No",
        "propertyVisited": "No",
        "hasFunds": "Yes",
        "hasPropertyInControlToManagementOrder": "No",
        "hasPropertyThatHasBeenRefused": "No"
      },
      "healthAndSafety": {
        "hasKitchenFireDoors": "No",
        "hasFireBlankets": "No",
        "hasFireExtinguishers": "No",
        "hasFireDetectionSystem": "Yes",
        "hasSafetyInformation": "Yes",
        "hasRegulationsCompliance": "Yes",
        "hasGasSupply": "No"
      },
      "propertyDetails": {
        "propertyUsage": "House in multiple occupation",
        "propertyStoriesAmount": 2,
        "floorsSituation": "Ground and first",
        "buildingStoriesAmount": 4,
        "propertyHouseholdAmount": 1,
        "propertyPeopleAmount": 4,
        "separateLettingsAmount": 1,
        "habitableRoomsAmount": 3,
        "propertyApproxYear": "Pre 1919",
        "externalStructures": "No"
      },
      "interestedParties": {
        "licenceHolder": "Jonny Smith",
        "personWhoCollectRent": "Jonny Smith",
        "applicant": "Jonny Smith",
        "parties": [
          {
            "title": "Mr",
            "firstName": "Jonny",
            "surname": "Smith",
            "companyName": "ESG Residential",
            "address": {
              "addressLine1": "1 Haberdasher Place",
              "addressLine2": "Church Lane",
              "city": "London",
              "country": "United Kingdom",
              "postcode": "N1 6BS"
            },
            "phoneNumber": "07399374613",
            "emailAddress": "jonny.smith6381@gmail.com",
            "partyType": "Freeholder",
            "organisation": true
          }
          ...
        ]
      },
      ...
      "dateDraftIssued": "2021-10-28T00:00:00+00:00",
      "dateFinalIssued": "2021-11-18T00:00:00+00:00",
      "dateValidFrom": "2021-11-18T00:00:00+00:00",
      "dateValidTo": "2026-11-17T00:00:00+00:00",
      "totalMaxPersons": 6,
      "totalMaxHouseholds": 2
    },
    ...
  ]
}
```




##### Returns a list of your licences. The licences are returned sorted by uprn, with the properties with the lowest uprn appearing first.

### Parameters

<p style="max-width:440px; margin-bottom:0; margin-left:28px; padding-top:15px; padding-left:0px; border-top-style:solid; border-top-color:#eee; border-top-width:1px">
<span style="font-size:13px; font-weight:700; color:#2a2f45; font-family:Menlo, Consolas, monospace">postcode</span> <span style="font-size:12px; font-weight:600; color:#8792a2">optional</span>
</p>

A filter on the list based on the licence’s postcode field. The value must be a string.  The filter is not case-sensitive and spaces can removed.

<p style="max-width:440px; margin-bottom:0; margin-left:28px; border-bottom-style:solid; border-bottom-color:#eee; border-bottom-width:1px"></p>

<p style="max-width:440px; margin-bottom:0; margin-left:28px; padding-top:15px; padding-left:0px; border-top-style:solid; border-top-color:#eee; border-top-width:1px">
<span style="font-size:13px; font-weight:700; color:#2a2f45; font-family:Menlo, Consolas, monospace">uprn</span> <span style="font-size:12px; font-weight:600; color:#8792a2">optional</span>
</p>

A filter on the list based on the licence’s uprn field. The value must be a string.

<p style="max-width:440px; margin-bottom:0; margin-left:28px; border-bottom-style:solid; border-bottom-color:#eee; border-bottom-width:1px"></p>

<p style="max-width:440px; margin-bottom:0; margin-left:28px; padding-top:15px; padding-left:0px; border-top-style:solid; border-top-color:#eee; border-top-width:1px">
<span style="font-size:13px; font-weight:700; color:#2a2f45; font-family:Menlo, Consolas, monospace">licenceTypeId</span> <span style="font-size:12px; font-weight:600; color:#8792a2">optional</span>
</p>

A filter on the list based on the licence’s licenceTypeId field. The value must be an integer.  Ids correspond to the following licence types:

id:`1` = `Mandatory HMO licence`</br>
id:`2` = `Additional HMO licence`</br>
id:`3` = `Selective licence`</br>
id:`4` = `Temporary Exemption`</br>
id:`5` = `257 HMO`</br>

<p style="max-width:440px; margin-bottom:0; margin-left:28px; border-bottom-style:solid; border-bottom-color:#eee; border-bottom-width:1px"></p>

<p style="max-width:440px; margin-bottom:0; margin-left:28px; padding-top:15px; padding-left:0px; border-top-style:solid; border-top-color:#eee; border-top-width:1px">
<span style="font-size:13px; font-weight:700; color:#2a2f45; font-family:Menlo, Consolas, monospace">licenceStatusId</span> <span style="font-size:12px; font-weight:600; color:#8792a2">optional</span>
</p>

A filter on the list based on the licence’s licenceStatusId field. The value must be an integer.  Ids correspond to the following licence statuses:

id:`1` = `Not-contacted`</br>
id:`2` = `Application created`</br>
id:`3` = `New`</br>
id:`4` = `2nd declaration - new`</br>
id:`6` = `2nd declaration - officer assigned`</br>
id:`7` = `2nd declaration - letter sent`</br>
id:`8` = `2nd declaration - no response`</br>
id:`9` = `2nd declaration - final reminder sent`</br>
id:`10` = `2nd declaration - no final response`</br>
id:`11` = `2nd declaration - complete`</br>
id:`12` = `Checks in progress`</br>
id:`13` = `Draft ready to send`</br>
id:`14` = `Draft sent`</br>
id:`15` = `Representation received`</br>
id:`16` = `Representation assessment`</br>
id:`17` = `Licence issued`</br>
id:`20` = `Licence revoked`</br>
id:`21` = `Licence refused`</br>
id:`22` = `Licence not required`</br>
id:`23` = `Checks not started`</br>
id:`24` = `2nd declaration - letter ready to send`</br>
id:`25` = `Final licence ready to send`</br>
id:`26` = `Make a decision`</br>
id:`27` = `Licence refusal letters ready to send`</br>
id:`28` = `Draft licence refusal sent`</br>
id:`29` = `Final refusal letter ready to send`</br>
id:`30` = `Refusal - Issue refund`</br>
id:`31` = `Representation received for licence refusal`</br>
id:`32` = `Representation assessment for licence refusal`</br>
id:`33` = `Revocation form received`</br>
id:`34` = `Revocation letters ready to send`</br>
id:`35` = `Draft revocation letters sent`</br>
id:`36` = `Final revocation letters ready to send`</br>
id:`37` = `Representation received for licence revocation`</br>
id:`38` = `Representation assessment for licence revocation`</br>
id:`39` = `Licence expired`</br>
id:`40` = `Variation form received`</br>
id:`41` = `Variation letters ready to send`</br>
id:`42` = `Final variation letters ready to send`</br>
id:`43` = `Draft variation letters sent`</br>
id:`44` = `Representation assessment for licence variation`</br>
id:`45` = `Representation received for licence variation`</br>
id:`46` = `Temporary exemption form received`</br>
id:`47` = `Temporary exemption not required`</br>
id:`48` = `TEN letters ready to send`</br>
id:`49` = `TEN issued`</br>
id:`50` = `TEN refused`</br>
id:`51` = `TEN expired`</br>
id:`52` = `Process Fee B charge`</br>
id:`53` = `New Renewal`</br>
id:`54` = `Renewal letters ready to send`</br>
id:`55` = `Renewal letters sent`</br>
id:`56` = `Application withdrawn`</br>
id:`57` = `Withdrawn - Issue refund`</br>





<p style="max-width:440px; margin-bottom:0; margin-left:28px; border-bottom-style:solid; border-bottom-color:#eee; border-bottom-width:1px"></p>

<p style="max-width:440px; margin-bottom:0; margin-left:28px; padding-top:15px; padding-left:0px; border-top-style:solid; border-top-color:#eee; border-top-width:1px">
<span style="font-size:13px; font-weight:700; color:#2a2f45; font-family:Menlo, Consolas, monospace">assigneeId</span> <span style="font-size:12px; font-weight:600; color:#8792a2">optional</span>
</p>

A filter on the list based on the licence’s assigneeId field. The value must be an integer.

<p style="max-width:440px; margin-bottom:0; margin-left:28px; border-bottom-style:solid; border-bottom-color:#eee; border-bottom-width:1px"></p>


<p style="padding-top:15px">
Pagination parameters are also available - see <a href="/?shell#pagination">Pagination</a>.
</p>


### Returns

<p style="max-width:440px; margin-bottom:15px; margin-left:28px; border-bottom-style:solid; border-bottom-color:#eee; border-bottom-width:1px"></p>

A dictionary with a `data` property that contains an array of licences.  Each entry in the array is a separate licence object. If no more licences are available, the resulting array will be empty. This request should never return an error.
