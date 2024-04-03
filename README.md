# Globus Tutorial

## Introduction

Globus is a cloud-based service designed for secure, reliable file transfer, sharing, and data management across various institutions. It is particularly useful for handling large datasets and comes equipped with tools like Globus Flows and Globus Compute to automate workflows and facilitate data analysis.

For more detailed informtion, please visit https://www.globus.org/

# Setting Up Globus

## Step 1: Log In with Your NYU Identity

This section explains how to log into Globus using an existing identity. 
Please log in with your NYU credentials, which is the first step in setting up your Globus access for secure and reliable file transfers and data sharing.

### Navigate to Globus

Go to [www.globus.org](https://www.globus.org/) and click on "Login" at the top of the page.

### Select Your Organization

On the Globus login page, start typing "New York University" in the search box to narrow down the list. When you find "New York University", click "Continue."
**Reminder:** Please ensure you select "Use your existing organizational login" and specifically avoid using "Sign in with Google" or other options.
![image](https://github.com/Yolo1105/Tutorial-on-globus/assets/99266347/f5aad530-be08-4c1e-828c-e3c00f66f6e8)


### Log In with NYU Credentials

You'll be redirected to NYU's login page. Use your NYU credentials to log in.

### Account Linking (Optional)

After logging in, Globus may prompt you about linking to an existing account.
   - If it's your first time using Globus, simply click "Continue."
   - If you've used Globus with another account, select "Link to an existing account." For more details, see the Identity Linking Tutorial provided by Globus.

### Complete the Sign-Up Process

You may be asked to provide additional information, such as your affiliation with NYU and whether or not you'll be using Globus for commercial purposes. Fill in the necessary details and proceed by clicking "Continue."

### Grant Globus Permission

Finally, Globus will request permission to use your identity for accessing information and performing actions (like file transfers) on your behalf. Granting this permission is essential for utilizing Globus services.

By following these steps, you will have successfully logged into Globus using your NYU identity. This initial setup is crucial for accessing the various services offered by Globus, including file transfers and data management.

![login-6](https://github.com/Yolo1105/Tutorial-on-globus/assets/99266347/62d84485-3c1a-476b-b41f-1afede2700c7)

## Step 2: Installing Globus Connect Personal (Optional)

Globus Connect Personal enables your personal computer to act as an endpoint for file transfers using Globus. Below are the unified steps to install Globus Connect Personal on macOS, Linux, and Windows systems, with specific instructions for each platform when needed.

### Prerequisites

Ensure you have a Globus account. If you don't, visit [Globus](https://www.globus.org/) and sign in to NYU credential.

### General Installation Steps

1. **Download the Installer:**
   - For **macOS** and **Windows**, visit the [Globus Connect Personal installation page](https://www.globus.org/globus-connect-personal) and select your operating system to download the installer.
   - For **Linux**, select your distribution on the [Linux installation page](https://docs.globus.org/globus-connect-personal/install/linux/) and download the appropriate installer.

2. **Install Globus Connect Personal:**
   - **macOS**: Open the downloaded file and follow the on-screen prompts.
   - **Linux**: Open a terminal, navigate to where you downloaded the installer, and follow the command-line installation instructions provided on the download page.
   - **Windows**: Execute the downloaded file and follow the installation prompts.

3. **Set Up an Endpoint:**
   - Once installed, launch Globus Connect Personal on your machine.
   - Follow the in-app instructions to log in with your Globus account.
   - Create a new endpoint, giving it a unique name for easy identification within the Globus ecosystem.

### Platform-Specific Guidance

- **macOS Users**: Access to certain folders may require granting additional permissions to Globus Connect Personal, especially for macOS Catalina and newer versions.
- **Linux Users**: The installation process may vary depending on your Linux distribution. Ensure you're following the guide corresponding to your version.
- **Windows Users**: Make sure to allow Globus Connect Personal through your firewall if prompted to ensure seamless file transfers.

### Post-Installation

After setting up Globus Connect Personal:

1. Log in to the [Globus Web App](https://app.globus.org/).
2. Use the File Manager to begin transferring files between your endpoint and others in the Globus network.
![image](https://github.com/Yolo1105/Tutorial-on-globus/assets/99266347/0cd07cd1-2ad5-4fc7-ad6c-29779bc09f50)


## Common Troubleshooting
![image](https://github.com/Yolo1105/Tutorial-on-globus/assets/99266347/a4f463b5-122e-4e65-8500-88596b3325ce)

### Issue: GTK+ Dependency or Non-GUI Preference

Installing Globus Connect Personal on Linux may require resolving GTK+ dependencies or accommodating a preference for non-GUI setups.

### Solutions

#### Installing GTK+ on Your System

1. **For Ubuntu/Debian-based Systems:**
   - If GTK+ is missing, install it by running the following commands in your terminal:
     ```sh
     sudo apt-get update
     sudo apt-get install libgtk2.0-0
     ```

#### Running Globus Connect Personal Without GUI

1. **Non-GUI Setup:**
   - If you prefer a CLI setup or if installing GTK+ does not resolve your issue, Globus Connect Personal can be installed without the GUI by using the following command:
     ```sh
     ./globusconnectpersonal -setup --no-gui
     ```

### Additional Tips

- Ensure your system meets all other prerequisites for running Globus Connect Personal.
- Distribution-specific instructions or requirements may apply. Check the Globus documentation for more information.
- For additional help and troubleshooting, refer to the [Globus documentation](https://docs.globus.org/globus-connect-personal/troubleshooting-guide/).


# Basic File Transfer with Globus
## Choose Your Source Endpoint
- After you’ve signed up and logged in to Globus, you’ll begin at the "File Manager" tab.
![filemgr-1](https://github.com/Yolo1105/Tutorial-on-globus/assets/99266347/9a6f183c-eff6-41fc-8076-fd5f21e7e211)
- The first time you use the File Manager, all fields will be blank.
![filemgr-2](https://github.com/Yolo1105/Tutorial-on-globus/assets/99266347/67121422-5fcb-4dd5-8b2f-71066c390bb9)

- Click in the Collection field at the top of the File Manager page and type "globus tutorial end". Globus will list collections with matching names. The collections Globus Tutorial Endpoint 1 and Globus Tutorial Endpoint 2 are collections administered by the Globus team for demonstration purposes and are accessible to all Globus users without further authentication.
![filemgr-3](https://github.com/Yolo1105/Tutorial-on-globus/assets/99266347/99fc7a98-5229-4209-8445-8ac160518764)

- Click on Globus Tutorial Endpoint 1. Globus will connect to the collection and display the default directory, /~/. (It will be empty.) Click the "Path" field and change it to /share/godata/. Globus will show the files in the new path: three small text files.
![filemgr-4](https://github.com/Yolo1105/Tutorial-on-globus/assets/99266347/f669f719-8df2-4670-b98b-9566fbb4c1fe)


## Getting Started with Collections to request a file transfer
### Key Concept: Collection

A **collection** is a fundamental concept within Globus, representing a named location where data is stored. Collections can be hosted on a wide variety of systems, enabling seamless data access and sharing across different storage environments. This guide provides an overview of what collections are and how they're used in Globus.

### What is a Collection?

A collection is essentially a pointer to a data storage location that has been named and integrated into the Globus ecosystem. These locations can vary widely, including but not limited to:

- Campus storage systems
- High-Performance Computing (HPC) clusters
- Personal laptops
- Cloud storage services like Amazon S3 and Google Drive
- Scientific instruments

The beauty of collections is that users interacting with Globus do not need to know the physical details or technical specifics of where the data is stored. To access or share data, you only need to know the collection's name.

### Uses of Collections

Collections serve multiple purposes within the Globus platform:

- **Data Access:** Collections allow authorized users to browse and transfer files seamlessly, regardless of the underlying storage infrastructure.
- **Data Sharing:** They provide a mechanism for sharing data with other Globus users, facilitating collaboration and data distribution.
- **Data Discovery:** Collections can be made discoverable to other Globus users, enhancing the visibility of datasets and promoting collaborative opportunities.

### Globus Connect and Collections

To host a collection, you'll need to use **Globus Connect**. Globus Connect comes in two flavors:

- **Globus Connect Personal:** For turning personal computers into Globus endpoints.
- **Globus Connect Server:** For integrating institutional storage systems, HPC clusters, and other large-scale storage into the Globus network.

By setting up Globus Connect, you can create collections on your storage systems, making your data accessible and shareable via the Globus platform.

1. Determine the storage system you wish to use with Globus.
2. Install the appropriate version of Globus Connect.
3. Create a collection and assign it a name for easy reference.
4. Configure access and sharing settings according to your needs.

### Navigate to the Files You Wish to Transfer

- Click Transfer or Sync to... in the command panel on the right side of the page. A new collection panel will open, with a "Transfer or Sync to" field at the top of the panel.
![filemgr-5](https://github.com/Yolo1105/Tutorial-on-globus/assets/99266347/42bb258f-89e1-4337-b1ee-3ec07f627d68)

- Find the Globus Tutorial Endpoint 2 collection and connect to it as you did with the Globus Tutorial Endpoint 1 above. The default directory, /~/ will again be empty. Your goal is to transfer the sample files here. Click on the left collection, Globus Tutorial Endpoint 1, and select all three files. The Start> button at the bottom of the panel will activate.
![filemgr-6](https://github.com/Yolo1105/Tutorial-on-globus/assets/99266347/f9986b74-1fc3-451f-8249-1aefe14d1f5b)

### Choose Your Destination Endpoint
- Between the two Start buttons at the bottom of the page, the Transfer & Sync Options tab provides access to several options. By default, Globus verifies file integrity after transfer using checksums. Click the information icons for explanations of the other transfer settings. Globus gives you powerful control over the behavior of the transfer with a simple mouse click. Change the transfer settings if you’d like. You may also enter a label for the transfer, but this isn’t required.

### Initiate the Transfer
- Click the Start> button to transfer the selected files to the collection in the right panel. Globus will display a green notification panel—​confirming that the transfer request was submitted—​and add a badge to the Activity item in the command menu on the left of the page.
![filemgr-7](https://github.com/Yolo1105/Tutorial-on-globus/assets/99266347/873417ff-5851-4503-9e53-dd20ea2142b4)

### Confirm transfer completion
- Only three small files were transferred in our simple example, so the transfer will complete quickly. Click Activity in the command menu on the left of the page to go to the Activity page. On the Activity page, click the arrow icon on the right to view details about the transfer. You will also receive an email with the transfer details.
![filemgr-8](https://github.com/Yolo1105/Tutorial-on-globus/assets/99266347/f5a2e9b3-f176-44f1-8d25-e55d66db962d)
![filemgr-9](https://github.com/Yolo1105/Tutorial-on-globus/assets/99266347/542504c7-711c-4131-b10b-dc893ec41a53)
- Click File Manager in the command menu on the left of the Activity page to return to the File Manager. The collections you were viewing before will reappear. You may notice that the transferred files are not listed in the right panel with the Globus Tutorial Endpoint 2 collection and the /~/ path, even though the transfer has completed. Click the refresh icon (circular arrows) at the top of the collection panel to see the updated contents.
![filemgr-10](https://github.com/Yolo1105/Tutorial-on-globus/assets/99266347/13ebc54e-b464-4e65-9857-662dc07e92c1)

# Sharing Data with NYU and Outside Entities
With Globus, you can easily share research data with your collaborators. You don’t need to create accounts on the server(s) where your data is stored. You can share data with anyone using their identity or their email address.

To share data, you’ll create a guest collection and grant your collaborators access as described in the instructions below. If you like, you can designate other Globus users as "access managers" for the guest collection, allowing them to grant or revoke access privileges for other Globus users.

## Step 1: Navigate to the Endpoint
- Select the collection that has the files/folders you wish to share and, if necessary, activate the collection.
![sharing-1](https://github.com/Yolo1105/Tutorial-on-globus/assets/99266347/faa64cd7-954f-4049-8aa1-fb8c829b0a9f)

## Step 2: Create or Use a Shared Endpoint

- Select the 'Share' option, set permissions, and invite users via their email addresses. Ensure outside users have a Globus account.
![sharing-2](https://github.com/Yolo1105/Tutorial-on-globus/assets/99266347/436d9331-4cf6-4d1f-b92f-d13547a57d22)
- If Share is not available, contact the endpoint’s administrator or refer to Globus Connect Server Installation Guide for instructions on enabling sharing. If you’re a using a Globus Connect Personal endpoint and you’re a Globus Plus user, enable sharing by opening the Preferences for Globus Connect Personal, clicking the Access tab, and checking the Sharable box.

## Step 3: Name and Create Your Collection
- Provide a name for your guest collection, such as "Demo," and click "Create Share." If this is your first time accessing the collection, authentication and consent for Globus services to manage your collections will be required.
![sharing-3](https://github.com/Yolo1105/Tutorial-on-globus/assets/99266347/4eb11963-9f55-4792-b7cc-107c545ce29f)


## Step 4: Setting Initial Permissions
- When your collection is created, you’ll be taken to the Sharing tab, where you can set permissions. As shown below, the starting permissions give read and write access (and the Administrator role) to the person who created the collection.
![sharing-4](https://github.com/Yolo1105/Tutorial-on-globus/assets/99266347/316ebc66-1153-4bdd-b247-f640abd027ba)

- Click the Add Permissions button or icon to share access with others. You can add permissions for an individual user, for a group, or for all logged-in users. In the Identity/E-mail field, type a person’s name or username (if user is selected) or a group name (if group is selected) and press Enter. Globus will display matching identities. Pick from the list. If the user hasn’t used Globus before or you only have an email address, enter the email address and click Add.
![sharing-5](https://github.com/Yolo1105/Tutorial-on-globus/assets/99266347/a1eef4dd-405e-426d-94ee-0ac49a872317)

## Step 5: Adding Permissions for Others
- To share access, click the "Add Permissions" button or icon. You can add permissions for an individual user, a group, or all logged-in users. In the "Identity/E-mail" field, enter the recipient's name, username, or group name and select the correct one from the matching identities presented by Globus.
![sharing-6](https://github.com/Yolo1105/Tutorial-on-globus/assets/99266347/15db43bd-95bf-403e-8afa-2efb43b700c7) 

## Step 6: Notification and Access Details
- If the user is new to Globus or if you have only their email address, enter it and click "Add." This grants the specified access level (e.g., read access) and sends an email notification to the user with a link to the shared endpoint. Optionally, add a customized message to this email. If you prefer not to send an email notification, uncheck the "Send E-mail" checkbox.
![sharing-5](https://github.com/Yolo1105/Tutorial-on-globus/assets/99266347/e2ce5a68-68ea-4674-b9ba-5d4c8ef741d9)

## Note on Write Access
Be aware that granting write access allows users to modify and delete files and folders within the specified folder.

## Step 7: Sharing Subfolders
- Permissions can also be set for subfolders by specifying a path in the "Path" field.
![sharing-6](https://github.com/Yolo1105/Tutorial-on-globus/assets/99266347/111150b6-8cf8-4893-91d6-0a14efd0a87d)


## Step 8: Accessing the Collection
- After receiving the email notification, your colleague can click on the link to log into Globus and access the guest collection. In the example below, user grohder1@globusid.org accesses the guest collection. Note that the collection name is Demo and the path is /, because this is what the user was given access to.
![sharing-7](https://github.com/Yolo1105/Tutorial-on-globus/assets/99266347/24a9b261-0029-45cb-adfa-aacd8f3eb499)

## Step 9: Managing Collection Permissions
To allow others to manage permissions, use the "Roles" tab. Here, you can assign roles, such as the "Access Manager," to individual users or groups, enabling them to manage permissions for the collection. The person who created the collection is assigned the "Administrator" role by default.
![sharing-8](https://github.com/Yolo1105/Tutorial-on-globus/assets/99266347/8f40dd61-0e0f-4026-950a-90dffca202cf)

## Step 10: Assigning the Access Manager Role
The "Access Manager" role can be granted to users, giving them the ability to manage collection permissions, including read/write access. For example, assigning this role to user "grohder1@globusid.org" enables them to manage permissions for others.
![sharing-9](https://github.com/Yolo1105/Tutorial-on-globus/assets/99266347/7dfcefb1-5cd9-4eff-be6e-5244376d9db7)

## Group Role Assignments
When a role is assigned to a group, all members of that group inherit the assigned role, streamlining permission management for teams or collaborative projects.

## Explore More About Managing Files with Globus
For detailed guidance on managing files, including transferring, sharing, and understanding the advanced functionalities of Globus, please visit https://docs.globus.org/guides/tutorials/manage-files/

# Globus Flows for Automated Data Management

## Run a Flow
Learn how to start a run of a flow using the Globus Flows service. Flows define reusable automations within the Globus ecosystem — and each time they are run, a run is created to track that execution.
The Run a Flow tutorial will walk you through starting a flow and supplying inputs to that flow to point it at your own Globus Collections.

### Open the Flows Page
- Login to the Globus Web App (app.globus.org) and open the Flows management page from the navigation menu.
![Flows_Navigation_Menu-2](https://github.com/Yolo1105/Tutorial-on-globus/assets/99266347/4cb920cb-fc68-4749-9a7c-5c1c4b43eea9)

### Navigate to the Run History and Flow Library
- When first-opened, the Flows management page displays your run history—including runs that are in progress. For now, select the Library tab to browse the flows available to you.
![Flows_Runs-Library_Tabs](https://github.com/Yolo1105/Tutorial-on-globus/assets/99266347/840825a2-20d1-4771-a7ed-c71b6608176b)

### Search for a Flow
- To find a specific flow, enter the name of the flow (or a portion of it) into the search field and press return. To follow this example, search for "two stage globus transfer."
![Flows_LibrarySearch-TwoStageTransfer-2](https://github.com/Yolo1105/Tutorial-on-globus/assets/99266347/1a89ede4-c559-4f7f-9614-37fd74328a6c)

### Tip
- You can further filter your search results using the Quick Filters below the search field.
![Flows_Library-Search-Quick-Filters](https://github.com/Yolo1105/Tutorial-on-globus/assets/99266347/a56b5e55-207e-4278-8d88-b2482f1b8cf4)

### Select a Flow to Run
- To open a flow’s Guided Input page, select the Start button next to the flow that you would like to run.
![Flows_Library-Select-Run-2](https://github.com/Yolo1105/Tutorial-on-globus/assets/99266347/fc02fa8f-1bd3-4a2f-900f-ff9cc87a929b)

### Set Run Parameters
- Most flows provide parameters that can be used to control aspects of what the flow does when it runs. On the Guided Input page, you can see a list of the parameters that this flow provides (you can use the Advanced tab if you prefer to provide JSON-formatted input).
- Choose your source, intermediate, and destination collections and paths. In this example, we’ll use the Globus Tutorial Endpoint collections (see below).
![Flows_Source-Intermediate-Destination_Selection-3](https://github.com/Yolo1105/Tutorial-on-globus/assets/99266347/583051f4-ab92-4139-aa27-1eb86a513767)

- Provide a name for this run using the Label This Run parameter.
<img width="367" alt="Flows_Run-Label" src="https://github.com/Yolo1105/Tutorial-on-globus/assets/99266347/724f4415-740e-4078-90bd-0f76fafb849c">


Notice that some of the parameters displayed in the Guided Input indicate that they are "[OPTIONAL]". These fields may safely ignored.
### Tip
In the Two Stage Globus Transfer flow, the "label" transfer parameters can be used to apply a custom label to the transfer operations that this flow will perform on your behalf. The "tags" parameters for the run are useful for keeping your run history organized.
![Flows_Run-Labels-And-Tags-2](https://github.com/Yolo1105/Tutorial-on-globus/assets/99266347/8a0e96d1-3d5b-473d-92f3-946dd3b48174)

### Start the Run
Once you’ve set all of the required parameters, the Start Flow button will become enabled. When you are ready, use this button to initiate a run of the Two Stage Globus Transfer flow.
![Flows_Run-Start](https://github.com/Yolo1105/Tutorial-on-globus/assets/99266347/88fb976b-e8bb-47bb-9f6e-e03e9fe11097)
Once the run has successfully launched, you should see the Run Successfully Started page, which displays your run’s label and unique ID.
![Flows_Run-StartedSuccessfully-2](https://github.com/Yolo1105/Tutorial-on-globus/assets/99266347/c203274b-5161-4aa2-a350-08c7c2bad540)

### Monitor Your Run’s Progress
- To view the details for your newly submitted Run, select View Run Details.
![Flows_Run-ViewRun](https://github.com/Yolo1105/Tutorial-on-globus/assets/99266347/f1a081fb-e0c6-4a07-8a84-669e5e2e2686)
- To view the status of all of your runs, select View All Runs.
![Flows_Run-ViewAllRuns-2](https://github.com/Yolo1105/Tutorial-on-globus/assets/99266347/903ac1f2-1aa0-424f-816d-fc9a288bd7d2)

### Next Steps
- For more information on monitoring runs, see: How to Monitor a Flow Run.
- You can also run flows via the Globus Automate CLI. If you are ready to create a flow, see How to Create a Flow to get started.

## Monitor a Run
Once you have learned How to Run a Flow, the next step is to learn how to monitor the progress of a run.
A run of a flow may be a long-running process. Some runs finish in minutes, but others may run for hours or even days.
The Run Monitoring tutorial will walk you through how to use the Globus Web App to check on the status of your runs and monitor them until completion.

## 1. Open the Flows Page
- Login to the Globus Web App (app.globus.org) and open the Flows management page from the navigation menu.
![Flows_Navigation_Menu-2](https://github.com/Yolo1105/Tutorial-on-globus/assets/99266347/a295dda2-2888-4dd4-a9f4-debdb077cca2)
- Use the Runs tab at the top if you need to return to this page later.
![Flows_Runs-Library_Tabs-RunsTab](https://github.com/Yolo1105/Tutorial-on-globus/assets/99266347/3e8d87e7-06ed-4f4c-a647-31bfb0870f3f)

## 2. Browse Your Runs
When first opened, the Flows management page displays your entire run history, including runs that are in progress.
![1-Flows_Monitoring_Run-List-All](https://github.com/Yolo1105/Tutorial-on-globus/assets/99266347/fe6084ee-5667-45cc-b79a-58f30ab09aea)

## 2.1. Sorting

To change the order runs are displayed in, reveal the sort options by selecting the Sort menu just above the runs list. You can sort runs alphabetically by their label, by when the flow was started, and by the name of the run’s flow.
![3-Flows_Monitoring_Run-Sorting-1](https://github.com/Yolo1105/Tutorial-on-globus/assets/99266347/84e24148-bf2a-4e83-a98f-44f0dba1aac3)

## 2.2. Searching

To search for a particular run label, use the search field (labeled "filter run list").
<img width="497" alt="Flows_Runs-Search" src="https://github.com/Yolo1105/Tutorial-on-globus/assets/99266347/fee2ded7-6752-4e59-a253-eea518d8f021">

## 2.3. Filtering
There are many options available to help focus on a specific subset of runs.
Quick Filters allow you to limit the view to only runs you started or runs in a particular state.
![3-Flows_Monitoring_Run-QuickFiltering-1](https://github.com/Yolo1105/Tutorial-on-globus/assets/99266347/a5489775-3349-489e-90eb-024f0e78edf1)

For even more options, including filtering by tags, select the Advanced Filters button.
![3-Flows_Monitoring_Run-AdvancedFiltering-2](https://github.com/Yolo1105/Tutorial-on-globus/assets/99266347/18640b05-cfe0-455c-8fa4-7838af0ebfbd)

## 3. Select a Run
To view the details of a particular run, select the run label from the list.
![3-Flows_Monitoring-Run-Selection-Label](https://github.com/Yolo1105/Tutorial-on-globus/assets/99266347/29960c7c-f84b-4852-a369-499c0ab9bcf6)

## 4. View Run Details
Selecting a run opens its details page. The Overview tab displays information about a run and the flow from which it was launched.
![4-Flows_Monitoring_Run-Overview-FailedRun](https://github.com/Yolo1105/Tutorial-on-globus/assets/99266347/ef624dec-f944-47d9-a7fa-bdafa1626a8b)

## 4.1. The Event Log
To examine the detailed execution history of the run, open the Event Log tab.
![4-Flows_Monitoring_Run-EventTab-FailedRun](https://github.com/Yolo1105/Tutorial-on-globus/assets/99266347/afd3ea30-346a-4be1-b3cb-1d5165298839)
Events are sorted chronologically, with the most recent events appearing at the top of the list. This view is updated as your run progresses.
## Note
The Event Log does not load additional events automatically as you scroll. If more events are available but not displayed, you can use the Load More button to reveal them.
![4-Flows_Monitoring_Run-EventTab-SuccessfulRun-LoadMoreEvents-1](https://github.com/Yolo1105/Tutorial-on-globus/assets/99266347/c2e0d195-caaa-4feb-ab66-5451dc64fd92)
## 4.2. Investigating a Run
In the example below, we can see the run has failed. To diagnose the cause of a failure, you can expand log entries to expose more detail. We can see that in this example, the run has indicated that the source path was missing.
![4-Flows_Monitoring_Run-EventTab-EventLog-1](https://github.com/Yolo1105/Tutorial-on-globus/assets/99266347/11c2d71a-6dcb-4f65-b5ae-d2a5b648e11a)
## The first entry in the run log—labeled FlowStarted and appearing at the bottom of the list—shows the original parameters that were provided as input for a run.
![4-Flows_Monitoring_Run-EventTab-EventLog-2](https://github.com/Yolo1105/Tutorial-on-globus/assets/99266347/461aea51-d8fd-423e-b6b4-831fe1c9c043)
## 4.3. Managing Roles
To collaborate with others, you can share access to runs with additional users and groups. To view existing permissions for a run, open the Roles tab.
<img width="241" alt="Flows_Runs-Roles-Tab" src="https://github.com/Yolo1105/Tutorial-on-globus/assets/99266347/02c9f9ed-305e-4274-9260-298dbca80326">
To grant access to another user, click the Assign New Role button.
![Flows_Runs-Assign-New-Role-3](https://github.com/Yolo1105/Tutorial-on-globus/assets/99266347/a1f5ee70-d490-4a29-a3be-678b6369ed8a)
On the Assign New Role page, you can search for a user or group and choose what type of access to grant.
![Flows_Runs-Assign-New-Role-UserSelection](https://github.com/Yolo1105/Tutorial-on-globus/assets/99266347/adedf8ea-8110-4484-9267-f99b317246f8)
![Flows_Runs-Assign-New-Role-RoleSelection](https://github.com/Yolo1105/Tutorial-on-globus/assets/99266347/1237dda3-6250-480b-b507-5d16bf61bf5e)

### 5. Next Steps
Globus also provides a command-line tool for starting and managing runs. For more information, see Globus CLI flows Command Reference.
If you’re ready to learn more about authoring your own flows, see How to Create a Flow.

## Create a Flow
Having covered the basics of running and monitoring flows, you may be interested in authoring flows of your own.
The Flow Creation tutorial covers the steps involved in defining your own flows.

### 1. Write a Flow Definition

A flow definition is a document that describes the actions that will occur when running a flow and the details necessary to perform them. Some steps in a flow — called actions — may interact with an action provider. Action providers can allow flows to access and modify resources within Globus or externally managed services.

You can incorporate Globus resources and capabilities in your flows by using Globus-provided action providers. You can also define and run your own custom action provider to expand the set of tools available to your flows.

A flow definition is a JSON document. These resources will help you get started with writing your flow definition:

    You can start experimenting by creating a simple flow to move and share data using our Jupyter notebook.

    You can use these example flow definitions as starting points for developing your own flows.

    You can access several simple flow definitions in this GitHub repository.

    You can view flow definitions that others have shared with you. To use one of these flow definitions to start building your own flow, login to the Globus Web App and select Flows from the navigation menu. Open the Library tab to find a flow you are interested in, selecting the flow to open up its Overview page. Open the Definition tab and expand the Definition section to view the flow’s definition. If you’d like to use this as the basis of a new flow, you can copy the definition and paste it into a new JSON file.

    Our flow authoring guide provides detailed instructions for how to write a flow definition.

The Globus CLI flows Command Reference provides a description of available CLI commands and their options.
### 2. Write an Input Schema

An input schema is a document that describes the settings (called parameters) which a user can provide to customize a run of a flow.

As with the flow definition, you will write and edit this file, only uploading it once you are ready to register your flow with Globus. We provide a guide for writing input schemas and sample input schemas to get you started.
### 3. Create the Flow

Once you have written your flow definition and input schema, you are ready to register your flow with the Globus Flows service.

You can use the Globus Web App to create your flow. Login to the Globus Web App (app.globus.org). Open the Flows page from the navigation menu, select the Deploy a Flow tab, and then select the Deploy Flow button.
![create_a_flow-1](https://github.com/Yolo1105/Tutorial-on-globus/assets/99266347/174c8de8-1c1b-4bcc-a82a-9e9ab9e4a14a)

Fill out the form and select the Deploy Flow button.
![create_a_flow-2](https://github.com/Yolo1105/Tutorial-on-globus/assets/99266347/6e5c6f1d-0587-4851-a2c7-8d5eab82c77e)


Alternatively, you can create your flow from the Globus CLI using the command:

$ globus flows create "FLOW_TITLE" FLOW_DEFINITION_FILE –-input-schema INPUT_SCHEMA_FILE

where FLOW_TITLE is the name of the flow, INPUT_SCHEMA_FILE is the file containing the flow's input schema, and FLOW_DEFINITION_FILE is the name of the file containing the flow definition.


### 4. Update the Flow and Set Flow Roles

Using the command below, you may update an existing flow's definition and input schema as well as metadata, such as the flow's title, keywords, and description. You may also use this command to assign roles, which determine who can see, run, or manage your flow. For a complete list of flow update options, see the globus flows update Reference.

$ globus flows update [OPTIONS] FLOW_ID

The Globus web application may also be used to update flow metadata and assign roles. To update a flow using the web application, select Flows from the navigation menu. In the Library tab, find your flow and select it to open the flow's Overview page.

### 5. Next Steps

Once you have created a flow, your next steps are probably to run it in order to test your work.

Refer back to the How to Run a Flow Tutorial for a description of how to run your flow.

## For further support, visit the [Globus Support](https://www.globus.org/support) page for detailed guides and troubleshooting assistance.

# Glow Compute
Please refer to this following link to get more detailed information on glow computing.
https://globus-compute.readthedocs.io/en/latest/quickstart.html
