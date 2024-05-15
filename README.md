# DevSum 2024 Pre-conf Workshop - Developing Solutions with GPT in Azure Open AI

# Links to slides and things mentioned during the workshop

Semantic Kernel presentation (and others)
https://github.com/jakobehn/presentations

Alans Inside GPT session
https://www.youtube.com/watch?v=2HFCd7tw-1w

Vectors comparision demo site
https://pamelafox.github.io/vectors-comparison/

Azure AI Search Lab (that you can deploy in your subscription)
https://github.com/jelledruyts/azure-ai-search-lab

# Guided Quickstarts & Tutorials

## Azure Open AI Service

**Quickstart**: Get started generating text using Azure OpenAI Service
Get started making your first calls to Azure OpenAI.
https://learn.microsoft.com/en-us/azure/ai-services/openai/quickstart

**Quickstart**: Get started using GPT-35-Turbo and GPT-4 with Azure OpenAI Service
Get started using Azure OpenAI.
https://learn.microsoft.com/en-us/azure/ai-services/openai/chatgpt-quickstart

**Quickstart**: Use images in your AI chats
Get started using GPT-4 Turbo with images with the Azure OpenAI Service.
https://learn.microsoft.com/en-us/azure/ai-services/openai/gpt-v-quickstart

**Quickstart**: Generate images with Azure OpenAI Service
Get started generating images with Azure OpenAI in your browser.
https://learn.microsoft.com/en-us/azure/ai-services/openai/dall-e-quickstart

**Quickstart**: Chat with Azure OpenAI models using your own data
Use your own data with Azure OpenAI models. Using Azure OpenAI's models on your data can provide you with a powerful conversational AI platform that enables faster and more accurate communication.
https://learn.microsoft.com/en-us/azure/ai-services/openai/use-your-data-quickstart

**Quickstart**: Get started using Azure OpenAI Assistants (Preview)
Azure OpenAI Assistants (Preview) allows you to create AI assistants tailored to your needs through custom instructions and augmented by advanced tools like code interpreter, and custom functions.
https://learn.microsoft.com/en-us/azure/ai-services/openai/assistants-quickstart

**Tutorial**: Explore Azure OpenAI Service embeddings and document search
This tutorial will walk you through using the Azure OpenAI embeddings API to perform document search where you'll query a knowledge base to find the most relevant document.
https://learn.microsoft.com/en-us/azure/ai-services/openai/tutorials/embeddings

**Azure OpenAI** speech to speech chat
In this how-to guide, you can use Azure AI Speech to converse with Azure OpenAI Service. The text recognized by the Speech service is sent to Azure OpenAI. The Speech service synthesizes speech from the text response from Azure OpenAI.
https://learn.microsoft.com/en-us/azure/ai-services/speech-service/openai-speech


## Semantic Kernal
This manual mainly focuses on the implementation of the Semantic Kernel version in .NET, Java and Python to get everyone started, and combines it with Azure OpenAI Service to provide guidance for everyone who needs to master the development of large model applications. T
https://github.com/microsoft/SemanticKernelCookBook

## LangChain
Build a chatbot to query your documentation using Langchain and Azure OpenAI
In this article, I will introduce LangChain and explore its capabilities by building a simple question-answering app querying a pdf that is part of Azure Functions Documentation.
https://techcommunity.microsoft.com/t5/startups-at-microsoft/build-a-chatbot-to-query-your-documentation-using-langchain-and/ba-p/3833134


## PromptFlow
Get started with PromptFlow
This article walks you through the main user journey of using prompt flow in Azure Machine Learning studio. You'll learn how to enable prompt flow in your Azure Machine Learning workspace, create and develop your first prompt flow, test and evaluate it, then deploy it to production.
https://learn.microsoft.com/en-us/azure/machine-learning/prompt-flow/get-started-prompt-flow?view=azureml-api-2


# Challenge Exercises

## Conference Presentation Proposal Generation
In this challenge exercise you will create a parameterized prompt that generates session titles and descriptions for conference presentations.
Implementation Details
Feel free to implement the solution as you wish, there are a number of alternatives:
- Experiment with prompts in OpenAI Studio
- A Python console application using LangChain.
- A C# console application using Semantic Kernel
- A C# or Python application calling the API directly.

## Experiment with Prompt Engineering
- Explement with a basic prompt to generate a session title and description.
- Think about the parameters that could be passed into the prompt, you could use the subject, technical level, target audience etc.
- Experiment with generating usable sessions by changing the wording in the prompt.

## Explore One and Few-Shot Generation
You can achieve more predictable results by providing one or more examples of how the session titles and descriptions should be formatted. Browse to https://www.devsum.se/agenda and choose a few sessions that you like the look of. Use one or more of these to  
- You may find that the descriptions include facts and technologies from the example sessions. Can you modify the prompt to prevent this?


## Chat with AI Whitepaper Documents
In this challenge exercise you will create a retrieval augmented generation (RAG) solution that will allow you to ask questions about GPT models.
The following Azure resources will be required:
- Azure Open AI Service
- Azure Storage Account
- Azure AI Search (Free or Basic tier is sufficient)

The following whitepapers would work well for this scenario:
- Attention Is All You Need – https://arxiv.org/abs/1706.03762
- Textbooks Are All You Need – https://arxiv.org/abs/2306.11644
- Harnessing the Power of LLMs in Practice: A Survey on ChatGPT and Beyond – https://arxiv.org/abs/2304.13712
- A Comprehensive Overview of Large Language Models – https://arxiv.org/abs/2307.06435

The high-level overview of the process is as follows:
- Ensure that you have the required Azure resources deployed.
- Browse to the Azure OpenAI Studio for your Azure Open AI service.
- ensure that you have a model deployment of gpt-35-turbo or gpt-4.
- On the Welcome page click Bring your own data.
- Add a data source by uploading your documents, select the storage and search services and the documents you would like to work with.
- Once the ingestion process is complete you should be able to ask questions related to the documents.
- Deploy the resource to an Azure website.
- Explore the index generated in Azure search.


## Orchestrate Plugins with Semantic Kernel
In this challenge you will extend an existing chat-based application that uses Semantic Kernel for AI orchestration. The application already contains some basic plugins, but your task is to create new plugins that will carry out some work for you. In doing this, you will learn both how to create and integrate a new native plugin in Semantic Kernel, and how to use prompt engineering to get the best results.

You can implement any plugin you want; we suggest that you don’t focus too much on the actual functionality of the plugin, but more on how to orchestrate the plugin using Semantic Kernel. Look at the existing plugins in the project for how native plugins are defined and integrated.

Here are some ideas for simple plugins that you could implement, in case you don’t come up with a cool idea yourself:
- A File plugin that can list, read, and write files from the local file system (there is actually a built-in one in Semantic Kernel, but this is a good exercise)

- A Swedish Radio API plugin, that can answer questions about programs aired on Swedish radio (hint, use the Orneholm.SwedishRadio.Api nuget package for communicating with the public API. See https://github.com/PeterOrneholm/Orneholm.SverigesRadio for examples)

Clone the following repository to get started https://github.com/ActiveSolution/devsum-ai-semantickernel.
You will need to update the appSettings.json file with the Azure OpenAI endpoint and credential information. Either use your own instance, or you can use service credentials provided by the workshop instructors.




