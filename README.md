# Globus Tutorial

## Introduction

Globus is a cloud-based service designed for secure, reliable file transfer, sharing, and data management across various institutions. Ideal for managing large datasets, Globus offers tools like Globus Flows and Globus Compute to automate workflows and facilitate data analysis.

## Setting Up Globus

### 1. Create a Globus Account

- Visit the [Globus website](https://www.globus.org/) and sign up using your institutional or personal email. NYU affiliates can use their NYU credentials.

### 2. Install Globus Connect Personal

- To transfer files from a personal computer, download and install Globus Connect Personal from the [official website](https://www.globus.org/globus-connect-personal).
- Follow the installation prompts, and set up an endpoint on your machine with a unique name.
- For Linux users, ensure GTK+ is installed using `sudo apt-get update` and `sudo apt-get install libgtk2.0-0` for Ubuntu/Debian systems. For a non-GUI setup, append `--no-gui` to the setup command.

### 3. Use Globus Connect Server for Institutional Servers

- For institutional servers or shared resources, your IT department will manage the setup of Globus Connect Server.

## Basic File Transfer with Globus

### 1. Log In

- Navigate to the Globus Web App and log in with your Globus account or institutional credentials.

### 2. Choose Your Source Endpoint

- Click on the "File Manager" tab and start typing the name of your personal computer's endpoint. Select it from the dropdown menu.

### 3. Navigate to the Files You Wish to Transfer

- Browse the directory structure to find the desired files or folders.

### 4. Choose Your Destination Endpoint

- Search and select the destination endpoint in the other panel. Authenticate if necessary.

### 5. Initiate the Transfer

- Select the files or folders and click "Start" or "Transfer". Monitor the progress in the "Activity" tab.

## Sharing Data with NYU and Outside Entities

### 1. Navigate to the Endpoint

- Go to the endpoint containing the data you wish to share.

### 2. Create or Use a Shared Endpoint

- Select the 'Share' option, set permissions, and invite users via their email addresses. Ensure outside users have a Globus account.

## Globus Flows for Automated Data Management

### 1. Access and Define Your Flow

- Log into the Globus Web App and navigate to the "Flows" service. Use the visual or JSON editor to define your flow, including actions, triggers, and conditions.

### 2. Activate the Flow

- Provide necessary input parameters, save, and enable the flow for automatic execution based on the defined conditions.

## Globus Compute for Data Analysis

### 1. Define Your Computing Task

- Specify the application to run, the input data, and the computing resources to use.

### 2. Transfer Input Data

- Use Globus to move input data to the computing resource.

### 3. Monitor the Task and Transfer Output Data

- Use Globus or the computing resource's tools to monitor the task. After completion, transfer the output data back to your desired location.

---

This tutorial outlines how to get started with Globus for file transfers, sharing data securely, and leveraging Globus' advanced features for automating data management and running analysis tasks on remote computing resources.
