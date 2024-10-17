
## Client Onboarding Integration

Integrating with the "Company" Platform for onboarding clients and members.

## Summary
This document aims to outline requirements and API integration endpoints required for onboarding a client and respective members onto the Reward Gateway Platform.

## Environments

<table style="border-radius: 10px";
              "border: 5px solid #154360";>
<tr>
<th>Environment</th>
<th>URL</th>
<tr>
<td>Testing:</td>
<td>https://api.testing.aws.company.net</td>
</tr>
<td>Production:	</td>
<td>https://api.company.net</td>
</tr>
</table>

## Prerequisites
The API integrations mentioned in this document require “Partner” level access to Reward Gateway. This MUST be requested from Reward Gateway prior to any integration that may occur.

Following successful partner onboarding, Reward Gateway will provide three key metadata required:


<ul>
<li>Partner Access Token</li>
<li>Partner Refresh Token</li>
<li>Unique Partner ID</li>
</ul>

## Onboarding a Client into Reward Gateway

Onboarding a client into Reward Gateway can be achieved by using the Reward Gateway REST API.

## Create a programme

### API


When a request for programme creation is sent, the response contains a programme status:

<ul>
<li>-1 - programme is not provisioned / not ready for use</li>
<li>0 - Implementation - programme is prepared for use and configuration</li>
<li>1 - Live - programme’s Reward Hub is accessible for members</li>
<li>2 - Closing - the programme is prepared to be closed after 60 days</li>
<li>3 - Closed - programme is not available</li>

Before using the programme, you should validate its status is different from -1. Use the following endpoint:

Retrieve programme details
Open Recipe
Add or replace the current domain attached to a programme (programme alise)

Update a programme's domain
Open Recipe
Edit programme details

Update a programme's details
Open Recipe

> [!NOTE]  
> Programme status can be changed only from implementation (0) to live (1), from live (1) to closing (2) and from closing (2) to closed (3). Other combinations are not allowed.

Programme Branding
Update a programme's logo
Open Recipe
Update a programme's branding color
Open Recipe
Onboarding a Member into a Reward Gateway Client
Onboarding members into Reward Gateway can be achieved by using the Reward Gateway SCIM API.
