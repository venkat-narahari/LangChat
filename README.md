# LangChat

## Overview

This project is an experiment to delve into LangChain and LLM application use cases using the Langchain library. The project focuses on generating detailed responses to user queries, demonstrated through an example.

## Setup

- Install langchain module to utilize Models from Hugging face to chain and prompt the models `!pip install langchain`.
- Generate an Access Token from Hugging Face.
  - Once logged into HuggingFace Go to [HuggingFace->Settings->AcessTokens](https://huggingface.co/settings/tokens)
  - Create a new access token and copy it or copy an existing token in read mode.
- Now go to Google Collab -> Secrets -> Create a new key HUGGINGFACE_ACCESS_TOKEN and add the access token here.
- Enable Notebook access so the notebook can use the access token to use hugging face models.

## Execution

- Once Setup is complete run the notebook.
- During the execution:
  1. LLM Model Setup
     - Imports
       - HuggingFaceHub: A class from Langchain for interacting with the Hugging Face Model Hub.
       - PromptTemplate: A class for creating templates for input prompts.
       - LLMChain: A class for chaining the Langchain modules.
       - UserData: A class for retrieves the secrets.
  2. Model Initialization:
     - HuggingFaceHub: Initializes a Hugging Face model using the specified repository ID (repo_id) and the provided Hugging Face API token.
     - model_kwargs: Additional keyword arguments passed to the model, such as randomness of the result and maximum new tokens.
  3. Prompt Template:
    - chat_template: A template defining the format of the chat, where there is a placeholder for the user's question.
    - PromptTemplate: Initializes a prompt template with the specified format and input variables.
Model Chaining:
  4. LLMChain: Chains the prompt template and the Hugging Face model to create a language model chain.
  5. Model Invocation: Invokes the chained model with a sample question. The question is provided as input to the model chain.
  6. Output: Once the model is invoked, a the response is generated and printed out.

- Notes:
  - Here [falcon-7b-instruct](https://huggingface.co/tiiuae/falcon-7b-instruct) Hugging face model is used.
  - You can replace with other hugging face alternative models and generate responses accordingly.


## Resources
- [Set up Google collab and drive with GitHub ](https://github.com/WiktorJ/google-colab-tutorial)
- [Langchain and Langchain Expression Language](https://python.langchain.com/docs/get_started)
- [Falcon 7b instruct Large Language Model](https://huggingface.co/tiiuae/falcon-7b-instruct)
- [The Falcon has landed in the Hugging Face ecosystem](https://huggingface.co/blog/falcon)

## License

This project is licensed under the MIT License.

Feel free to learn, fork and merge the project. 
