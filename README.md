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
- For further support, visit the [Globus Support](https://www.globus.org/support) page for detailed guides and troubleshooting assistance.


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

## Confirm transfer completion
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



# Globus Flows for Automated Data Management

### Access and Define Your Flow

- Log into the Globus Web App and navigate to the "Flows" service. Use the visual or JSON editor to define your flow, including actions, triggers, and conditions.

### Activate the Flow

- Provide necessary input parameters, save, and enable the flow for automatic execution based on the defined conditions.

## Globus Compute for Data Analysis

### Define Your Computing Task

- Specify the application to run, the input data, and the computing resources to use.

### Transfer Input Data

- Use Globus to move input data to the computing resource.

### Monitor the Task and Transfer Output Data

- Use Globus or the computing resource's tools to monitor the task. After completion, transfer the output data back to your desired location.

This tutorial outlines the steps to get started with Globus for file transfers, sharing data securely, and leveraging Globus' advanced features for automating data management and running analysis tasks on remote computing resources.
