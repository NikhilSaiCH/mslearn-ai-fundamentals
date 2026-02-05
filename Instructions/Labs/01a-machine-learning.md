# Explore Automated Machine Learning in Azure Machine Learning

## Lab overview

In this lab, you will use browser-based Machine Learning Lab to create a workspace, train a regression model using Automated Machine Learning, deploy the best-performing model, and test it using sample input data. This lab demonstrates how automated machine learning simplifies model development and deployment without requiring extensive coding.

## Lab Objectives

In this lab, you will perform:

- Task 1: Creating an Azure Machine Learning workspace resource
- Task 2: Use automated machine learning to train a model
- Task 3: Deploy the model
- Task 4: Test the deployed service

### Task 1: Create an Azure Machine Learning workspace

In this task, you will create and open a Machine Learning Lab workspace that will be used throughout the lab to store datasets, run automated machine learning jobs, and deploy models.

1. Open the **Browser-based ML Lab** by navigating to [https://aka.ms/ml-lab](https://aka.ms/ml-lab) in your web browser, and wait for the environment to load.

    >**Note:** Do not refresh or close the web browser while using ML Lab, as doing so will reset the session and all unsaved work will be lost.

2. On the **Machine Learning Lab** home page, select **Create workspace (1)**. In the **Create a new workspace** pane, enter the required details, and then click **Create (4)**.

    - Name : **AI-900-Workspace-<inject key="DeploymentID" enableCopy="false" />** **(3)**
    - Resource group : **AI-900-Module-01** **(2)**
 
        ![Picture1](media/lab01n-e1t1p1.png)

3. On the **Machine Learning Lab** page, click the workspace you created to open it.

   ![Picture1](media/lab01n-e1t1p2.png)

4. Open a new browser tab and download the dataset from **[https://aka.ms/mslearn-ml-data](https://aka.ms/mslearn-ml-data)**. Extract the downloaded **ml-data.zip** file to view its contents. One of the extracted files, **ice-cream.csv**, contains the ice cream sales data needed for this exercise.
  
## Validation

> **Congratulations** on completing the task! Now, it's time to validate it. Here are the steps:
> - Hit the Validate button for the corresponding task. If you receive a success message, you can proceed to the next task.
> - If not, carefully read the error message and retry the step, following the instructions in the lab guide. 
> - If you need any assistance, please contact us at cloudlabs-support@spektrasystems.com. We are available 24/7 to help you out.

  <validation step="0e571ab6-2856-478e-afa3-41efc38df116" />

### Task 2: Use automated machine learning to train a model

In this task, you will create an Automated ML regression job, upload a dataset, select the target column, configure evaluation metrics and limits, and submit the job for training.

1. On the Machine Learning Lab page, navigate to the **Automated ML (1)** page (under **Authoring**), select  **+ New Automated ML job (2)**.

   ![](media/lab01n-e1t1p3.png)  

1. On the **Submit an Automated ML job** page, provide the following details: 

    **Basic settings**:

    - **Job name**: mslearn-icecream-automl **(1)**
    - **Description**: Automated machine learning for ice cream demand prediction **(2)**
    - Click **Next (3)**

       ![](media/lab01n-e1t1p4(1).png)

   **Task type & data**:

    - **Task type**: Regression **(1)**
    - Click on **Create (Tabular) (2)** 

        ![](media/lab01n-e1t1p4.png)

    - Scroll down to create new data with the following settings:

        - **Dataset name**: `ice-cream` **(1)**
        - **Upload CSV file**:  click on **Choose File** **(2)** and upload the `ice-cream.csv` file that you have downloaded and extracted in the previous task.
        - Uncheck the **Date** column **(3)** (*Date* is unique for each row, and adds little predictive capability on its own). Make sure only these column are selected.
            - **DayOfWeek**
            - **Month**
            - **Temperature**
            - **Rainfall**
            - **IceCreamsSold**
        - review columns, then click **Create (4)**

            ![](media/lab01n-e1t1p5.png)
      
        - After the dataset is created, select the **ice-cream (1)** dataset to continue to submit the Automated ML job. Select **Next (2)**

          ![](media/lab01n-e1t1p6.png)
        
    **Task settings**:

    - **Target column**: IceCreamsSold **(1)**
    - Select **View additional configuration settings (2)** under Target Column:
        - Primary metric: **R2** **(3)**
        - Leave everything else as default and then click on **Save (6)**.

            ![](media/lab01n-e1t1p7.png)

    - **Limits**: **Expand this section**
        - Use the limits to end the training job early based on specific criteria. In this exercise, set the following limits:
          - Metric score threshold: **0.9** **(1)**
          - Experiment Timeout (minutes): **15** **(2)**
          - Click **Next (3)**

            ![](media/lab01n-e1t1p8.png)

            >**Note:** It's important to set these limits when using Azure Machine Learning, as running training jobs for every possible algorithm and featurization combination could potentially take hours.

    **Compute**:
    - **Select compute type**: Serverless **(1)**
    -  Select **Next (2)**

        ![](media/lab01n-e1t1p9.png)

1. Select **Submit**. It starts automatically.

   ![](media/lab01n-e1t1p10.png)

1. Wait for the job to complete. This process should take only a few minutes at maximum.

**Review the best model**

When the automated machine learning job has completed, you can review the best model it trained.

1. On the **Overview** tab of the automated machine learning job, note the best model summary.

    ![](media/lab01n-e1t1p11.png)
  
1. Select the text beside **Algorithm name** for the best model to view its details.

    ![](media/lab01n-e1t1p12.png)

  - **Overview:** General details for the child job.

    ![](media/lab01n-e1t1p13.png)

  - **Model:** Information about the model that was trained.

    ![](media/lab01n-e1t1p14.png)

  - **Metric:** Select the **Metrics** tab to view the model performance metrics and related visualizations.

    ![](media/lab01n-e1t1p15.png)

  - **Outputs and logs:** Information logged during the training process.

    ![](media/lab01n-e1t1p16.png)

### Task 3: Deploy and test the model

In this task, you will deploy the trained model using default deployment settings and monitor the deployment status until it succeeds.

1. On the **Model** tab for the best model from your automated machine learning job, select **Deploy (1)**. Leave the settings as default, review them in the **Deploy model** pane, and then click **Deploy (2)**.

      ![](media/lab01n-e1t1p17.png)

1. Wait until the **Deploy status** shows *Succeeded*. This process may take a few minutes.

1. On the **Model has been successfully deployed!** pop-up window, click on **Okay**.

    ![](media/lab01n-e1t1p18.png)

### Task 4: Test the deployed service

In this task, you will test the deployed endpoint by submitting sample JSON input and reviewing the predicted output.

1. In Machine Learning Labs page, on the left hand menu, select **Endpoints (1)** under Assets section and click on the **Endpoint (2)**.

    ![](media/lab01n-e1t1p19.png)

1. On the *endpoint* page, click on the **Test** tab.

    ![](media/lab01n-e1t1p20.png)

1. In the **Input data (JSON)** pane, replace the template JSON with the following input data **(1)**:

    ```json
    {
    "input_data": {
        "columns": [
            "DayOfWeek",
            "Month",
            "Temperature",
            "Rainfall"
        ],
        "index": [0],
        "data": [["Wednesday","June",70.5,0.05]]
     }
    }
    ```

1. Click the **Send Test Request (2)** button.

    ![](media/lab01n-e1t1p21.png)

1. Review the test results, which include a predicted number of ice creams sold based on the input features - similar to this:

    ```JSON
    [
      121.98976731059767
    ]
    ```

    ![](media/lab01n-e1t1p22.png)

    The test pane took the input data and used the model you trained to return the predicted number of ice creams sold.

Let’s review what you have done. You used a dataset of historical ice cream sales data to train a model. The model predicts the number of ice creams expected to be sold on a given day, based on seasonal and meteorological features.

### Review

In this lab, you created a Machine Learning Lab workspace, trained a regression model using Automated ML, evaluated model performance, deployed the best model as an endpoint, and tested it with real input data. These steps illustrate an end-to-end machine learning workflow for building and operationalizing predictive solutions.
  
## You have successfully completed this lab.
