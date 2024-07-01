
## Endpoint for Postman 
<br>http://ua-1185-mysql-system-api.us-e2.cloudhub.io/SpaceXdbService/SpaceXdbServiceSoapPort</br>

## Endpoint for SoapUI
<br>http://0.0.0.0:8081/SpaceXdbService/SpaceXdbServiceSoapPort</br>

## Input Create Launch
```xml
<soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/" xmlns:roc="http://example.com/rocketservice">
   <soapenv:Header/>
   <soapenv:Body>
      <roc:CreateLaunchRequest>
         <externalId>LN10</externalId>
         <success>0</success>
         <details>Unsuccessful cargo resupply mission.</details>
         <launchName>Cargo Mission 8</launchName>
         <date>2023-03-23</date>
         <rocketName>Falcon 3</rocketName>
         <launchpad_id>2</launchpad_id>
      </roc:CreateLaunchRequest>
   </soapenv:Body>
</soapenv:Envelope>
```
## Input Create Launchpad
```xml
<soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/" xmlns:roc="http://example.com/rocketservice">
   <soapenv:Header/>
   <soapenv:Body>
      <roc:CreateLaunchpadRequest>
         <externalId>LP8</externalId>
         <name>Launchpad 8</name>
         <locality>Locality 8</locality>
         <region>Region 8</region>
         <status>Active</status>
      </roc:CreateLaunchpadRequest>
   </soapenv:Body>
</soapenv:Envelope>
```

## Input Create Rocket 
```xml
<soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/" xmlns:roc="http://example.com/rocketservice">
   <soapenv:Header/>
   <soapenv:Body>
      <roc:CreateRocketRequest>
         <externalId>RKT10</externalId>
         <name>Vega-1</name>
         <active>0</active>
         <stages>5</stages>
         <costPerLaunch>5500000.00</costPerLaunch>
         <description>An expendable launch system used for heavy payloads.</description>
      </roc:CreateRocketRequest>
   </soapenv:Body>
</soapenv:Envelope>
```

## Input Create Payload
```xml
<soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/" xmlns:roc="http://example.com/rocketservice">
   <soapenv:Header/>
   <soapenv:Body>
      <roc:CreatePayloadRequest>
            <externalId>PLD11</externalId>
		  <name>Starlink-1</name>
		  <type>Communications</type>
		  <weight>260</weight>
		  <orbit>LEO</orbit>
		  <apoapsis>550</apoapsis>
		  <periapsis>550</periapsis>
		  <rocketId>2</rocketId>
      </roc:CreatePayloadRequest>
   </soapenv:Body>
</soapenv:Envelope>
```
## Output Create 

```xml
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
   <soap:Body>
      <body>
         <soap:Result xmlns:soap="http://schemas.xmlsoap.org/soap/envelope">
            <message>Created successfully</message>
         </soap:Result>
      </body>
   </soap:Body>
</soap:Envelope>
```

## Input Update Launch
```xml
<soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/" xmlns:roc="http://example.com/rocketservice">
   <soapenv:Header/>
   <soapenv:Body>
      <roc:UpdateLaunchRequest>
         <externalId>LN10</externalId>
         <success>1</success>
         <details>Successful cargo resupply mission.</details>
         <launchName>Cargo Mission 8</launchName>
         <date>2023-03-24</date>
         <rocketName>Falcon 3</rocketName>
      </roc:UpdateLaunchRequest>
   </soapenv:Body>
</soapenv:Envelope>
```
## Input Update Launchpad
```xml
<soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/" xmlns:roc="http://example.com/rocketservice">
   <soapenv:Header/>
   <soapenv:Body>
      <roc:UpdateLaunchpadRequest>
         <externalId>LP3</externalId>
         <name>Launchpad 3</name>
         <locality>Locality 4</locality>
         <region>Region 5</region>
         <status>Active</status>
      </roc:UpdateLaunchpadRequest>
   </soapenv:Body>
</soapenv:Envelope>
```
## Input Update Rocket
```xml
<soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/" xmlns:roc="http://example.com/rocketservice">
   <soapenv:Header/>
   <soapenv:Body>
      <roc:UpdateRocketRequest>
         <externalId>RKT5</externalId>
         <name>Vega-2</name>
         <active>0</active>
         <stages>5</stages>
         <costPerLaunch>5500000.00</costPerLaunch>
         <description>An expendable launch system used for heavy payloads.</description>
      </roc:UpdateRocketRequest>
   </soapenv:Body>
</soapenv:Envelope>
```
## Input Update Payload
```xml
<soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/" xmlns:roc="http://example.com/rocketservice">
   <soapenv:Header/>
   <soapenv:Body>
      <roc:UpdatePayloadRequest>
         <externalId>?</externalId>
         <name>?</name>
         <type>?</type>
         <weight>?</weight>
         <orbit>?</orbit>
         <apoapsis>?</apoapsis>
         <periapsis>?</periapsis>
      </roc:UpdatePayloadRequest>
   </soapenv:Body>
</soapenv:Envelope>
```
## Output Update
```xml
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
   <soap:Body>
      <body>
         <soap:Result xmlns:soap="http://schemas.xmlsoap.org/soap/envelope">
            <message>Updated successfully</message>
         </soap:Result>
      </body>
   </soap:Body>
</soap:Envelope>
```
## Input for Delete
```xml
<soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/" xmlns:roc="http://example.com/rocketservice">
   <soapenv:Header/>
   <soapenv:Body>
      <roc:DeleteLaunchByExternalIdRequest>
         <externalId>?</externalId>
      </roc:DeleteLaunchByExternalIdRequest>
   </soapenv:Body>
</soapenv:Envelope>

<soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/" xmlns:roc="http://example.com/rocketservice">
   <soapenv:Header/>
   <soapenv:Body>
      <roc:DeleteLaunchpadByExternalIdRequest>
         <externalId>?</externalId>
      </roc:DeleteLaunchpadByExternalIdRequest>
   </soapenv:Body>
</soapenv:Envelope>

<soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/" xmlns:roc="http://example.com/rocketservice">
   <soapenv:Header/>
   <soapenv:Body>
      <roc:DeleteRocketByExternalIdRequest>
         <externalId>?</externalId>
      </roc:DeleteRocketByExternalIdRequest>
   </soapenv:Body>
</soapenv:Envelope>

<soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/" xmlns:roc="http://example.com/rocketservice">
   <soapenv:Header/>
   <soapenv:Body>
      <roc:DeletePayloadByExternalIdRequest>
         <externalId>?</externalId>
      </roc:DeletePayloadByExternalIdRequest>
   </soapenv:Body>
</soapenv:Envelope>
```
## Output for Delete
```xml
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
   <soap:Body>
      <body>
         <soap:Result xmlns:soap="http://schemas.xmlsoap.org/soap/envelope">
            <message>Deleted successfully</message>
         </soap:Result>
      </body>
   </soap:Body>
</soap:Envelope>
```
## Input for GET

```xml
<soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/" xmlns:roc="http://example.com/rocketservice">
   <soapenv:Header/>
   <soapenv:Body>
      <roc:GetLaunchByExternalIdRequest>
         <externalId>?</externalId>
      </roc:GetLaunchByExternalIdRequest>
   </soapenv:Body>
</soapenv:Envelope>

<soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/" xmlns:roc="http://example.com/rocketservice">
   <soapenv:Header/>
   <soapenv:Body>
      <roc:GetLaunchpadByExternalIdRequest>
         <externalId>?</externalId>
      </roc:GetLaunchpadByExternalIdRequest>
   </soapenv:Body>
</soapenv:Envelope>

<soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/" xmlns:roc="http://example.com/rocketservice">
   <soapenv:Header/>
   <soapenv:Body>
      <roc:GetRocketByExternalIdRequest>
         <externalId>?</externalId>
      </roc:GetRocketByExternalIdRequest>
   </soapenv:Body>
</soapenv:Envelope>

<soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/" xmlns:roc="http://example.com/rocketservice">
   <soapenv:Header/>
   <soapenv:Body>
      <roc:GetPayloadByExternalIdRequest>
         <externalId>?</externalId>
      </roc:GetPayloadByExternalIdRequest>
   </soapenv:Body>
</soapenv:Envelope>
```
## Output for GET Launch
```xml
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
   <soap:Body>
      <roc:GetLaunchByExternalIdResponse xmlns:roc="http://example.com/rocketservice">
         <id>12</id>
         <externalId>LN10</externalId>
         <success>true</success>
         <details>Successful cargo resupply mission.</details>
         <launchName>Cargo Mission 8</launchName>
         <date>2023-03-24</date>
         <rocketName>Falcon 3</rocketName>
         <launchpad_id>2</launchpad_id>
      </roc:GetLaunchByExternalIdResponse>
   </soap:Body>
</soap:Envelope>
```
## Output for GET Launchpad
```xml
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
   <soap:Body>
      <roc:GetLaunchpadByExternalIdResponse xmlns:roc="http://example.com/rocketservice">
         <id>8</id>
         <externalId>LP8</externalId>
         <name>Launchpad 8</name>
         <locality>Locality 8</locality>
         <region>Region 8</region>
         <status>Active</status>
      </roc:GetLaunchpadByExternalIdResponse>
   </soap:Body>
</soap:Envelope>
```
## Output for GET Rocket
```xml
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
   <soap:Body>
      <roc:GetRocketByExternalIdResponse xmlns:roc="http://example.com/rocketservice">
         <id>5</id>
         <externalId>RKT5</externalId>
         <name>Vega-2</name>
         <active>false</active>
         <stages>5</stages>
         <costPerLaunch>5500000</costPerLaunch>
         <description>An expendable launch system used for heavy payloads.</description>
      </roc:GetRocketByExternalIdResponse>
   </soap:Body>
</soap:Envelope>
```
## Output for GET Launchpad
```xml
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
   <soap:Body>
      <pay:GetPayloadByExternalIdResponse xmlns:pay="http://example.com/rocketservice">
         <id>1</id>
         <externalId>PLD1</externalId>
         <name>Starlink-1</name>
         <type>Communications</type>
         <weight>260</weight>
         <orbit>LEO</orbit>
         <apoapsis>550</apoapsis>
         <periapsis>550</periapsis>
         <rocketId>2</rocketId>
      </pay:GetPayloadByExternalIdResponse>
   </soap:Body>
</soap:Envelope>
```



