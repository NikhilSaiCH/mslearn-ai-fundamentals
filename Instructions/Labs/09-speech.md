<<<<<<< HEAD
---
lab:
    title: 'Explore Speech in Azure AI Foundry portal'
---

# Explore Speech in Azure AI Foundry portal
=======
# Module 09 : Explore Speech in Azure AI Foundry portal

## Lab overview
>>>>>>> 20a06afb6504d7ebfb91f217980cf0897bf34e2e

The **Azure AI Speech** service transcribes speech into text, and text into audible speech. You might use AI Speech to create an application that can transcribe meeting notes or generate text from the recording of interviews.

In this exercise, you will use Azure AI Speech in Azure AI Foundry portal, Microsoft's platform for creating intelligent applications, to transcribe audio using the built-in try-it-out experiences. 

<<<<<<< HEAD
## Create a project in Azure AI Foundry portal

1. In a web browser, open the [Azure AI Foundry portal](https://ai.azure.com) at `https://ai.azure.com` and sign in using your Azure credentials. Close any tips or quick start panes that are opened the first time you sign in. 

1. In the browser, navigate to `https://ai.azure.com/managementCenter/allResources` and select **Create**. Then choose the option to create a *new Azure AI Foundry resource*.

1. In the *Create a project* wizard, enter a valid name for your project.

1. Expand *Advanced options* to specify the following settings for your project:
    - **Subscription**: Your Azure subscription
    - **Resource group**: Create or select a resource group
    - **Region**: Select one of the following locations:
        * East US
        * France Central
        * Korea Central
        * West Europe
        * West US

    Wait for your project and hub to be created.

1. When the project is created, you will be taken to an *Overview* page of the project details.
 
1. On the left-hand menu on the screen, select **Playgrounds**.

1. On the *Playgrounds* page, select the **Speech playground** tile to try out some Azure AI Speech capabilities.

## Explore speech to text in Azure AI Foundry's Speech Playground

Let's try out *speech to text* in Azure AI Foundry's Speech Playground. 

1. On the *Speech* page, scroll down and select **Real-time transcription** under *Try out Speech capabilities*. You will be taken to the *Speech Playground*. 
=======
## Lab objectives

In this lab, you will perform:

- Task 1: Create a project in the Azure AI Foundry portal
- Task 2: Explore speech to text in Azure AI Foundry's Speech Playground

### Task 1: Create a project in the Azure AI Foundry portal

In this task, we are creating and configuring a project in Azure AI Foundry to explore AI services and speech capabilities.

1. Right-click on the [Azure AI Foundry](https://ai.azure.com?azure-portal=true) **(1)** link, select **Copy link (2)** from the context menu, then paste it into a new tab to access the Azure AI Foundry portal.
>>>>>>> 20a06afb6504d7ebfb91f217980cf0897bf34e2e

   ![](./media/3-27.png)

<<<<<<< HEAD
1. Under *Upload files*, select **Browse files** and navigate to the folder where you saved the file. Select **WhatAICanDo.m4a** and then **Open**.
=======
1. On the Welcome to Azure AI Foundry page, Click on **Sign in** in the top right corner.

   ![](./media/17-18.png)

1. If prompted to sign in, enter your credentials:
>>>>>>> 20a06afb6504d7ebfb91f217980cf0897bf34e2e

   - **Email/Username:** <inject key="AzureAdUserEmail"></inject>
 
      ![Enter Your Username](./media/19-4.png)
 
   - **Password:** <inject key="AzureAdUserPassword"></inject>
 
     ![Enter Your Password](./media/19-5.png)
 
1. If prompted to stay signed in, you can click **No**.

   ![](./media/9-8.png)

1. If prompted with *Streamlined from the start*, click on **Got it** to proceed.

   ![](./media/3-23.png)

1. On the Azure AI Foundry portal home page, select **Create a project**. In Azure AI Foundry, projects are containers that help organize your work.  

    ![Screenshot of Azure AI Foundry home page with create a project selected.](./media/azure-ai-foundry-create-project.png)

1. On the **Create a project** pane, enter project name **Myproject<inject key="DeploymentID" enableCopy="false" /> (1)** and then select **Customize (2)**.

    ![](./media/17-3.png)

1. On the **Create a project** pane, Configure it with the following settings:

    - **Hub name**: Enter **myhub<inject key="DeploymentID" enableCopy="false" /> (1)**
    - **Subcription**: **Use existing Azure subscription (2)**
    - **Resource group**: Select **AI-900-Module-09 (3)**
    - **Location**: Select **<inject key="location" enableCopy="false"/> (4)**
    - **Connect Azure AI Services or Azure OpenAI Service**:
    Click on **Create new AI Services (5)** and provide name **AI<inject key="DeploymentID" enableCopy="false" /> (6)** and click on **Next**
    - **Connect Azure AI Search**: Leave as default **(7)**
    - Click on **Next (8)**

        ![](./media/9-19.png)

    > **Important**: You will need an Azure AI services resource provisioned in a specific location to complete the rest of the lab.

1. On the **Review and Finish** page, click on **Create**.

    ![](./media/9-9.png)

1. Keep track of the following created resources: 
    
    - **Azure AI Project**
    - **Azure AI Hub**  
    - **Azure AI Services**    
    - **Storage Account**  
    - **Key Vault**

      ![](./media/17-4.png)

1. If prompted with Explore and experiment, click on **Close** to dismiss it.

1. On the **AI Services (1)** page, select the **Speech (2)** tile to try out Azure AI Speech capabilities.

   ![](./media/up1.png)

> **Congratulations** on completing the task! Now, it's time to validate it. Here are the steps:
 
- Hit the Validate button for the corresponding task. If you receive a success message, you can proceed to the next task. 
- If not, carefully read the error message and retry the step, following the instructions in the lab guide.
- If you need any assistance, please contact us at cloudlabs-support@spektrasystems.com. We are available 24/7 to help you out.

   <validation step="a78cde3c-b21b-4ea4-9230-2d5a5d655239" />

### Task 2: Explore speech to text in Azure AI Foundry's Speech Playground

In this task, we are using Azure AI Speech to transcribe audio into text in real time using the Speech Playground.

Let's try out *real time speech to text* in Azure AI Foundry's Speech Playground. 

1. On the *Speech* page, scroll down and select **Real-time transcription** under *Try out Speech capabilities*. You will be taken to the *Speech Playground*. 

   ![](./media/9-6.png)

1. Copy highlighted link by right-clicking the [**https://aka.ms/mslearn-speech-files**](https://aka.ms/mslearn-speech-files) and selecting "Copy" from the context menu and paste it into the new tab to download **Speech.zip**. 

1. Click the **download icon (1)** to view your downloads, then click the **folder icon (2)** to open the file location.

   ![](./media/9-2.png)

1. **Right-click** the **ZIP file (1)**  and select **Extract All (2)** to **unzip** its contents. 

   ![](./media/9-3.png)

1. Select the destination folder, ensure Show extracted files when complete is checked, and click **Extract** to unzip the files. 

   ![](./media/9-4.png)

1. The Speech folder contains **m4a** file named **WhatAICanDo**. 

   ![](./media/9-5.png)

1. Go back to the Azure AI Foundry portal, select Connected resource **(1)**, click **Browse files (2)** to upload the **WhatAICanDo.m4a** file, navigate to **C:\Users\azureuser\Downloads\Speech (3)**, select **WhatAICanDo (4)**, and click **Open (5)** to begin transcription.

   ![](./media/9-7.png)

   > **Note:** If you're unable to see the resource, click the **three dots (1)** and select **Connected resource (2)** to choose the appropriate resource.

      ![](./media/9-10.png)

1. The Speech service transcribes and displays the text in real time. If you have audio on your computer, you can listen to the recording as the text is being transcribed.
<<<<<<< HEAD

1. Review the output, which should have successfully recognized and transcribed the audio into text.

In this exercise you tried out Azure AI Speech services in Azure AI Foundry's Speech Playground. You then used Real-time transcription to transcribe an audio recording. You were able to see the text transcription being generated as the audio file was played.
=======

1. The output successfully transcribes the audio, capturing how AI enhances various aspects of life, including healthcare, accessibility, infrastructure, entertainment, and environmental sustainability.

   ![Browse files](media/9-1.png)
>>>>>>> 20a06afb6504d7ebfb91f217980cf0897bf34e2e

### Review

<<<<<<< HEAD
If you don't intend to do more exercises, delete any resources that you no longer need. This avoids accruing any unnecessary costs.
=======
In this exercise, you have completed the following tasks:
>>>>>>> 20a06afb6504d7ebfb91f217980cf0897bf34e2e

- Explored Azure AI Speech services in the Speech Playground
- Transcribed audio to text using the Real-time speech-to-text service

## Learn more

<<<<<<< HEAD
This exercise demonstrated one of the many capabilities of the Speech service. To learn more about what you can do with this service, see the [Speech page](https://azure.microsoft.com/services/cognitive-services/speech-services).
=======
This exercise demonstrated only some of the capabilities of the Speech service. To learn more about what you can do with this service, see the [Speech page](https://azure.microsoft.com/services/cognitive-services/speech-services).

## You have successfully completed this lab.
>>>>>>> 20a06afb6504d7ebfb91f217980cf0897bf34e2e
