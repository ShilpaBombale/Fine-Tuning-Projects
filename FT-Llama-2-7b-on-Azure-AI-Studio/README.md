# Step-by-Step Guide to Fine-Tuning LLaMA 2 7B on Azure AI Studio

This project demonstrates the fine-tuning of LLaMA 2 7B on Azure AI Studio for IC Automation.

This guide provides a detailed, step-by-step process to fine-tune the LLaMA 2 7B model on Azure AI Studio. By following this guide, you'll learn how to set up your environment, configure the fine-tuning task, and deploy the fine-tuned model.

## Prerequisites

- **Azure account**: You'll need an active Azure subscription.
- **Basic knowledge of machine learning**: Familiarity with concepts like model fine-tuning and deployment.

## 1. Create a Resource Group in Azure Portal

1. **Access Azure Portal**:
    - Open your web browser and navigate to [Azure Portal](https://portal.azure.com/).
    - Log in with your Azure credentials.

2. **Create a Resource Group**:
    - In the left-hand menu, select **Resource groups**.
    - Click on the **+ Create** button.
    - Enter the following details:
      - **Subscription**: Select your Azure subscription.
      - **Resource group**: Enter a name, e.g., `AzureML`.
      - **Region**: Select `West US 3` or any supported region.
    - Click **Review + create**, then **Create** once validation passes.

## 2. Set Up Azure AI Studio

1. **Navigate to Azure AI Studio**:
    - In the Azure Portal, use the search bar to find **Azure AI Studio**.
    - Click on **Azure AI Studio** and click **Create** to set up a new workspace.

2. **Create a New Workspace**:
    - In the "Basics" tab, provide the necessary details:
      - **Subscription**: Select your Azure subscription.
      - **Resource group**: Choose the resource group you created earlier (e.g., `AzureML`).
      - **Workspace name**: Enter a name, e.g., `AzureML-Demo`.
      - **Region**: Select `West US 3`.
    - Click **Review + create**, and once validated, click **Create**.

3. **Open Azure AI Studio**:
    - Once your workspace is created, go to the resource and click **Launch studio**.

## 3. Create and Configure the Project

1. **Create a New Project**:
    - In Azure AI Studio, navigate to the **Projects** section.
    - Click **+ New project**, provide a name, and click **Create**.

https://github.com/user-attachments/assets/d8a0607c-e15a-46c4-aa64-b3bda5a1c834

## 4. Fine-Tune the Model

1. **Navigate to Fine-tuning**:
    - In Azure AI Studio, go to the **Tools** section and select **Fine-tuning**.

2. **Select the Model to Fine-Tune**:
    - Choose the **LLaMA 2 7B** model from the list of available models.
    - Follow the prompts to configure fine-tuning settings.

3. **Upload Your Dataset**:
    - Select the task type, e.g., **Text Generation**.
    - Upload your `data.jsonl` file by following the prompts.
    - Map the labels to **Prompt** and **Completion** for text generation tasks.

https://github.com/user-attachments/assets/7735cef6-0711-4a31-9774-a88ce4e207bf

4. **Upload Validation Data (Optional)**:
    - You can optionally upload a separate validation dataset, or let the tool split your dataset into training and validation sets.
      

5. **Set Task Parameters**:
    - For new users, it’s recommended to keep default settings:
        - **Batch Size Multiplier**
        - **Learning Rate**
        - **Epochs**
    - More experienced users can adjust these parameters to fit their specific needs.

6. **Submit the Fine-Tuning Job**:
    - Review and submit the job. The training will start, and you can monitor its progress.

https://github.com/user-attachments/assets/4ed7fe6a-45a9-47fc-b390-9293541515e6

## 5. Evaluate the Fine-Tuned Model

1. **View Training Results**:
    - After the job completes, view the fine-tuning metrics and evaluate model performance.

https://github.com/user-attachments/assets/35299379-0ff4-4ea8-aa22-04a534767441

## 6. Deploy the Fine-Tuned Model

1. **Deploy the Model**:
    - Click on **Deploy** and follow the prompts to configure the deployment.
    - Give your deployment a unique name, then click **Deploy**. The process may take a few moments.
  
https://github.com/user-attachments/assets/4f35acc9-d208-4fac-9842-9a116d569d9d

## 7. Post-Deployment Steps

1. **Access API**:
    - Once the deployment is complete, locate the **Endpoint URL** and **API Key**.
    - Use these to make API requests. Tools like Postman can be used to test the API.

2. **Monitor Performance**:
    - Set up monitoring to track performance and usage using Azure’s built-in tools.
      
https://github.com/user-attachments/assets/f5a74a72-ee2b-4433-88ef-cb7075890ab8

## 8. Optimize and Iterate

1. **Adjust Fine-Tuning Parameters**:
    - Based on model performance, adjust fine-tuning parameters and iterate to improve performance if needed.

## 9. Delete Unused Deployments

1. **Why Delete?**
    - Unused deployments may incur additional costs. Azure bills based on resource usage, so it's recommended to delete deployments you no longer need.

2. **How to Delete**:
    - Navigate to the Azure Portal and find the deployed resource.
    - Select the deployment and click **Delete**.
    - Optionally, verify all associated resources are removed, or delete the entire resource group.

## Pricing

Azure charges for fine-tuning and deploying the LLaMA 2 7B model based on usage. Ensure to review the pricing details on the [Azure Pricing page](https://azure.microsoft.com/en-us/pricing/).

