# ACME System1 Automation Library

This UiPath library automates interactions with the ACME System1 website. It handles various operations such as logging in and out, navigating to work items, extracting and updating work item details, and updating the comment and status of each work item. This library can serve as a reusable component for automating workflows related to the ACME System1 website.

## Features
- Login and logout from the ACME System1 website
- Navigate to the Work Items page
- Extract a list of available work items
- Navigate to individual work item pages
- Extract detailed information from each work item
- Update work item comments and status

## Prerequisites
- UiPath Studio (latest version)
- A compatible web browser (Chrome/Firefox)
- UiPath Web Automation packages installed
- Stable internet connection
- Valid credentials for the ACME System1 website

## Installation
1. Download or clone this repository:
   ```bash
   git clone https://github.com/yourusername/uipath-acme-system1-automation.git
2. Open UiPath Studio and load the library into your project.

## Usage
1. Import the Library: After cloning or downloading, import the library into your UiPath project.
2. Setup Credentials: Ensure that your ACME System1 login credentials are stored securely, either using UiPath Orchestrator Assets or Windows Credential Manager.
3. Use Activities: Use the following sequence of activities to automate ACME System1 operations:
   - Login: Automates logging into the ACME System1 website.
   - Navigate to Work Items: Directs the browser to the Work Items page.
   - Extract Work Items: Scrapes data about all work items from the page.
   - Navigate to Individual Work Item: For each work item, this navigates to its detail page.
   - Extract Work Item Details: Captures information such as work item ID, type, description, etc.
   - Update Work Item: Automates navigating to the update page, where it changes the comment and status fields for each work item.
   - Logout: Logs out from the system.

## Example Workflow
1. Login: Pass the username and password as input arguments or store them securely using Orchestrator Assets or Credential Manager.
2. Navigate and Extract: After logging in, navigate to the Work Items page and extract the available work items.
3. Iterate through Work Items: For each work item:
   - Navigate to the work item detail page.
   - Extract details such as item ID, description, and type.
   - Navigate to the update page and update the status and comment fields.
4. Logout: Once all work items are processed, log out from the ACME System1 website.

## Customization
- Browser Type: The library is set to use Chrome by default. You can modify the browser type in the Open Browser activity if required.
- Selector Updates: Depending on any UI changes to the ACME System1 website, you may need to adjust the selectors for navigating or extracting work item details.
  
## Error Handling
- Proper exception handling is built into the activities to ensure that the process continues even if a particular work item cannot be processed.
- If the login fails, the process will retry a set number of times before exiting.

## Contributions
Feel free to submit issues or pull requests to enhance the library.
