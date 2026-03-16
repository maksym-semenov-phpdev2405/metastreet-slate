## Retrieve a licence

> <span style="font-family:Consolas, Menlo, Monaco, \"Lucida Console\", \"Liberation Mono\", \"DejaVu Sans Mono\", \"Bitstream Vera Sans Mono\", \"Courier New\", monospace, serif"><span style="color:#a4cdfe">GET</span> /licences/:referenceNo</span>

```shell
$ curl 'https://your_council.metastreet.co.uk/api/v1.1/licences/YCO-58348491339' \
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
      "assignedOfficer": {
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



##### Retrieves a Licence object.  Supply the unique Licence Reference Number (`referenceNo`) in the URL and Metastreet will return the corresponding licence information.

### Parameters

<p style="max-width:440px; margin-bottom:0; margin-left:28px; padding-top:15px; padding-left:0px; border-top-style:solid; border-top-color:#eee; border-top-width:1px">
<span style="font-size:12px; color:#8792a2;">No parameters.</span>
</p>


### Returns

<p style="max-width:440px; margin-bottom:15px; margin-left:28px; border-bottom-style:solid; border-bottom-color:#eee; border-bottom-width:1px"></p>

Returns the Licence object for a valid identifier.
