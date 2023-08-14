# UiPath-CalculateClientSecurityHash

## Description
This repository contains automation processes to interact with the ACME System 1 Web Application using UiPath. The process involves performing various tasks related to calculating client security hashes for specific work items.

## Steps

### Step 1.1 - Open ACME System 1 Web Application
Open the ACME System 1 Web Application to initiate the automation process.

### Step 1.2 - Log in to System 1
Provide the required input data, including email and password, to log in to System 1.

### Step 1.3 - Access the Dashboard
Access the Dashboard, which serves as a central location for users to select specific menu items.

### Step 1.4 - Access Work Items Listing
Access the Work Items listing to view all available tasks that need to be performed. Output data: Work Items.

### Step 1.5 - For Each WI5 Activity
For each activity of type WI5, perform the following steps:

#### Step 1.5.A - Open Activity Details
Open the Details page of the selected activity to retrieve the Client Details.

#### Step 1.5.B - Generate SHA1 Hash
Open the SHA1 generator webpage of your choice, for example https://codebeautify.org/sha1-hash-generator, and provide the following input:
- ClientID
- ClientCountry

Replace all the variables with the corresponding values. Use dashes between each item and the above.

#### Step 1.5.C - Retrieve Client Security Hash
Retrieve the Client Security Hash value from the webpage.

#### Step 1.5.D - Update Work Item
Go back to Work Item Details and open Update Work Item.

#### Step 1.5.E - Set Status to "Completed"
Set the status of the Work Item to "Completed" and add a comment with the obtained Security Hash.

### Step 1.6 - Continue with Next WI5 Activity
Continue with the next WI5 Activity in the list.

## Automation Components

- Dispatcher Robot: This component is responsible for managing the process and initiating the necessary actions.
- Performer Robot: This component is built using the REFramework and handles the execution of tasks for calculating client security hashes.


## Supervision
This project has been done under the supervision of **ADVANSYS-ESC**, providing guidance and support throughout the development process.

