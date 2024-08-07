# Overview
This Splunk Technology Add-on (TA) leverages Microsoft Graph's List-application endpoint to collect comprehensive details on Azure Application Registrations, providing valuable insights into your Azure environment.

### Key Features
- Azure Application Data Collection
    - Utilize the `List-application` endpoint from Microsoft Graph to gather detailed information about your Azure Application Registrations. See more details about this Graph endpoint [here.](https://learn.microsoft.com/en-us/graph/api/application-list)
- Monitoring Capabilities
    - This add-on allows you to monitor changes and detect possible abuses of Azure Application or Client IDs, helping to enhance your security posture.
- Optional Query Parameters
    - For Graph experts, append your Query Parameters!

### Requirements
- Azure Application/Client ID with permission
    - `Application.Read.All`

### Recommendations
- Infrequent Collection
    - To optimize performance and efficiency, it is recommended to schedule data collection as infrequently as possible, ideally once per day.

### Benefits
- Enhanced Visibility
    - Gain a clearer view of your Azure Application Registrations and their changes over time.
- Security Monitoring
    - Detect and respond to potential abuses or unauthorized changes to your Azure Applications and Client IDs.

### Installation and Configuration
- Download and Install
    - Obtain the TA package and install it on your Splunk instance.
- Configuration
    - Under Configurations tab, create a new Global account and enter under the `Username` field the Client ID and `Password` field the Client Secret
    - Under the Inputs tab, click `Create New Input` button
        - Enter a unique name for under the Name field
        - Under interval, enter the number of seconds for this collection's frequency, e.g. 86400 (for once per day)
        - Select Index, Client ID
        - Enter the Tenant or Directory ID associated with your Client
        - For experts, modify the response of Graph by appending Query Parameters

### Support
My favourite beer is IPA and would happy to have one today. Send me some 🤗 : daniel.l.astillero@gmail.com