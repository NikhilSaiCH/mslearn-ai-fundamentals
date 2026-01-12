# AI-900: Microsoft Azure AI Fundamentals Workshop

Welcome to your AI-900: Microsoft Azure AI Fundamentals workshop! We've prepared a seamless environment for you to explore and learn Azure Services. Let's begin by making the most of this experience.

# Detect faces in Vision Studio

### Overall Estimated timing: 30 Minutes

## Overview

In this hands-on lab, you'll gain practical experience in using Azure AI services to detect human faces in images with Vision Studio. You will learn how to create and configure an Azure AI Services resource, connect it to Vision Studio, and utilize Azure AI Face to analyze images. By following step-by-step tasks, you’ll explore how to detect facial features, identify bounding box coordinates, and analyze partially obscured faces. By the end of this lab, you'll be proficient in setting up and using Vision Studio for face detection, equipping you with the skills to leverage Azure AI for computer vision applications in real-world scenarios.

## Objectives

By the end of this lab, you will be able to detect human faces in images using Azure AI Face through Vision Studio.

1. **Create an Azure AI Services resource:**
You will learn how to create an Azure AI Services multi-service resource in the Azure portal to enable access to Azure AI Face capabilities.

2. **Connect Azure AI Services resource to Vision Studio:** You will learn how to associate an existing Azure AI Services resource with Vision Studio to enable face detection features.

3. **Detect faces using Vision Studio:** You will learn how to use Vision Studio to detect human faces in images and view bounding box information.

## Pre-requisites

Basic knowledge of Azure AI services and Speech service.

## Architecture

In this hands-on lab, the architecture flow includes several essential components.

1. **Provision an Azure AI multi-service resource:** Learn how to create a centralized Azure AI Services resource in the Azure portal that provides access to Azure AI Face capabilities. This includes configuring settings such as subscription, resource group, region, and pricing tier required to enable face detection features.

1. **Explore and test face detection using Vision Studio:** Use Vision Studio to connect to the Azure AI Services resource and interact with Azure AI Face features. This includes uploading images, detecting human faces, and viewing bounding box coordinates through a graphical interface without writing code.

## Architecture Diagram

![An image](../media/lab-04.PNG)

## Explanation of Components

1. **Vision Studio:** A web-based platform used to explore Azure AI Vision capabilities through a graphical interface. It enables testing of face detection features by analyzing images without requiring code.

1. **Azure AI Services Resource (Face):**
A multi-service Azure AI resource that provides access to Azure AI Face capabilities. It processes images submitted from Vision Studio and returns face detection results such as bounding box coordinates.

# Getting Started with lab
 
Welcome to your AI-900: Microsoft Azure AI Fundamentals workshop! We've prepared a seamless environment for you to explore and learn about machine learning and AI concepts and related Microsoft Azure services. Let's begin by making the most of this experience:
 
## Accessing Your Lab Environment
 
Once you're ready to dive in, your virtual machine and **Guide** will be right at your fingertips within your web browser.
 
![Access Your VM and Lab Guide](../media/4-7.png)

### Virtual Machine & Lab Guide
 
Your virtual machine is your workhorse throughout the workshop. The lab guide is your roadmap to success.

## Exploring Your Lab Resources
 
To get a better understanding of your lab resources and credentials, navigate to the **Environment** tab.
 
![Explore Lab Resources](../media/aig2.png)

## Lab Guide Zoom In/Zoom Out
 
To adjust the zoom level for the environment page, click the **A↕: 100%** icon located next to the timer in the lab environment.

![](../media/zoomintab.png)

## Utilizing the Split Window Feature
 
For convenience, you can open the lab guide in a separate window by selecting the **Split Window** button from the Top right corner.
 
![Use the Split Window Feature](../media/aig3.png)

## Managing Your Virtual Machine
 
Feel free to **start, stop, or restart (2)** your virtual machine as needed from the **Resources (1)** tab. Your experience is in your hands!
 
![Manage Your Virtual Machine](../media/aig4.png)

## Lab Duration Extension

1. To extend the duration of the lab, kindly click the **Hourglass** icon in the top right corner of the lab environment. 

    ![Manage Your Virtual Machine](../media/gext.png)

    >**Note:** You will get the **Hourglass** icon when 10 minutes are remaining in the lab.

2. Click **OK** to extend your lab duration.
 
   ![Manage Your Virtual Machine](../media/gext2.png)

3. If you have not extended the duration prior to when the lab is about to end, a pop-up will appear, giving you the option to extend. Click **OK** to proceed.

## Let's Get Started with Azure Portal
 
1. On your virtual machine, click on the Azure Portal icon as shown below:
 
   ![Launch Azure Portal](../media/sc900-image(1).png)

2. You'll see the **Sign into Microsoft Azure** tab. Here, enter your **credentials (1)** and click on **Next (2)**:
 
   - **Email/Username:** <inject key="AzureAdUserEmail"></inject> 
 
       ![Enter Your Username](../media/sign-in-page.png)
 
3. Next, provide your **password (1)** and click on **Sign in (2)**:
 
   - **Password:** <inject key="AzureAdUserPassword"></inject> 
 
       ![Enter Your Password](../media/tap-password.png)
 
4. If you see the pop-up Stay-Signed in?, click **No**.

    ![](../media/Sign-in-no.png)

5. If a **Welcome to Microsoft Azure** pop-up window appears, simply click **Cancel**.

    ![](../media/AI-l6-4.png)

## Support Contact
 
The CloudLabs support team is available 24/7, 365 days a year, via email and live chat to ensure seamless assistance at any time. We offer dedicated support channels explicitly tailored for both learners and instructors, ensuring that all your needs are promptly and efficiently addressed.
 
Learner Support Contacts:
 
- Email Support: cloudlabs-support@spektrasystems.com
- Live Chat Support: https://cloudlabs.ai/labs-support

Click on **Next** from the lower right corner to move on to the next page.

   ![Start Your Azure Journey](../media/sc900-image(3).png)

## Happy Learning !!
