# ACME System1 Automation Library

This UiPath library automates interactions with the [ACME System1 website](https://acme-test.uipath.com/). It handles various operations such as logging in and out, navigating to work items, extracting and updating work item details, and updating the comment and status of each work item. This library can serve as a reusable component for automating workflows related to the ACME System1 website.

## Features
- Login and logout from the ACME System1 website
- Navigate to the Work Items page
- Extract a list of available work items
- Navigate to individual work item pages
- Extract detailed information from each work item
- Update work item comments and status

## Prerequisites
- UiPath Studio (latest version)
- A compatible web browser (Chrome)
- UiPath Web Automation packages installed
- Stable internet connection
- Valid credentials for the ACME System1 website

## Installation
1. Download or clone this Library:
3. Open UiPath Studio and load the library into your project.

## Usage
![Library](https://github.com/mnsy1/UiPath_ACMESystem1/blob/main/img/ACMESystem1.png)
1. Import the Library: After cloning or downloading, import the library into your UiPath project.
2. Setup Credentials: Ensure that your ACME System1 login credentials are stored securely, either using UiPath Orchestrator Assets or Windows Credential Manager.
3. Use Activities: Use the following sequence of activities to automate ACME System1 operations:
   - Login: Automates logging into the ACME System1 website.
   - Navigate to Work Items: Directs the browser to the Work Items page.
   - Extract Work Items: Scrapes data about all work items from the page.
   - Navigate to Details Page: For each work item, this navigates to its detail page.
   - Extract Data from Details Page: Captures information such as Client ID, Account Number, Account Amount.
   - Click Update Work Item Button: Clicks on the Update Work Item Button to open the update page.
   - Update Work Item: Automates navigating to the update page, where it changes the comment and status fields for each work item.
   - Logout: Logs out from the system.

## Example Workflow
1. Login: Pass the username and password as input arguments or store them securely using Orchestrator Assets or Credential Manager.
![Login](https://github.com/mnsy1/UiPath_ACMESystem1/blob/main/img/ACMESystem1_Login.png)
2. Navigate and Extract: After logging in, navigate to the Work Items page and extract the available work items.
- Navigate To Work Items
- Extract Work Items
![Extract Work Items](https://github.com/mnsy1/UiPath_ACMESystem1/blob/main/img/Extract_Work_Items.png)
3. Iterate through Work Items: For each work item:
   - Navigate to the work item detail page.
![Navigate to Details Page](https://github.com/mnsy1/UiPath_ACMESystem1/blob/main/img/Navigate_to_Details_Page.png)
   - Extract details such as Client ID, Account Number, and Account Amount.
![Extract Data from Details Page](https://github.com/mnsy1/UiPath_ACMESystem1/blob/main/img/Extract_Data_from_Details_Page.png)
   - Navigate to the update page and update the status and comment fields.
![Click Update Work Item](https://github.com/mnsy1/UiPath_ACMESystem1/blob/main/img/Click_Update_Work_Item.png)
![Update Work Item](https://github.com/mnsy1/UiPath_ACMESystem1/blob/main/img/Update_Work_Item.png)
5. Logout: Once all work items are processed, log out from the ACME System1 website.
![Logout](https://github.com/mnsy1/UiPath_ACMESystem1/blob/main/img/ACMESystem1_Logout.png)

## Customization
- Browser Type: The library is set to use Chrome by default.
- Selector Updates: Depending on any UI changes to the ACME System1 website, the Library will adjust the selectors for navigating or extracting work item details.
  
## Error Handling
- Proper exception handling is built into the activities to ensure that the process continues even if a particular work item cannot be processed.
- If the login fails, the process will retry a set number of times before exiting.

## Contributions
Feel free to submit issues or pull requests to enhance the library.
