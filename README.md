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

# Use Globus Connect Server for Institutional Resources

If you need to transfer files to or from institutional servers or shared resources, your institution's IT department typically manages these setups through Globus Connect Server. Contact them for access and instructions.

## Next Steps

After setting up Globus Connect Personal:

1. Log in to the [Globus Web App](https://app.globus.org/).
2. Use the File Manager to start transferring files between your newly created endpoint and others within the Globus ecosystem.

For more detailed instructions and troubleshooting, refer to the official [Globus documentation](https://docs.globus.org/).



## Basic File Transfer with Globus

### Choose Your Source Endpoint

- Click on the "File Manager" tab and start typing the name of your personal computer's endpoint. Select it from the dropdown menu.

### Navigate to the Files You Wish to Transfer

- Browse the directory structure to find the desired files or folders.

### Choose Your Destination Endpoint

- Search and select the destination endpoint in the other panel. Authenticate if necessary.

### Initiate the Transfer

- Select the files or folders and click "Start" or "Transfer". Monitor the progress in the "Activity" tab.

## Sharing Data with NYU and Outside Entities

### Navigate to the Endpoint

- Go to the endpoint containing the data you wish to share.

### Create or Use a Shared Endpoint

- Select the 'Share' option, set permissions, and invite users via their email addresses. Ensure outside users have a Globus account.

## Globus Flows for Automated Data Management

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
