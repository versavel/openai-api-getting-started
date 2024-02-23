# OpenAI platform API

## Getting started with the OpenAI platform API

Use the following instructions to start a conversation with GPT in a Jupyter notebook. The notebook interacts with the OpenAI platform using their API. It's a basic example of what the OpenAI platform API has to offer. There are links to more information about the OpenAI platform at the bottom of this document.

### Get API key
Using the OpenAI platform requires an account and subscription to use the API. After signing up [here](https://platform.openai.com/signup), download an API key [here](https://platform.openai.com/api-keys).

### Install Docker 
[on MacOS](install_docker_macos.md)  
[on Ubuntu 22.04](install_docker_ubuntu.md)

### Download this repo
Open a new terminal window and clone the repository as follows
```
git clone git@github.com:versavel/openai-api-getting-started.git
```
### Enter your API key
Go the the directory where you installed the repo, for example
```
cd openai-api-getting-started
```
And then enter the /jovyan directory
```
cd jovyan
```
Create a file called "key" and enter your API key in the file. Make sure the file contains only the key symbols and no extra lines or spaces.

### Launch a Jupyter notebook server
Go back to the directory where you installed the repo, for example
```
cd openai-api-getting-started
```
and run the following command to launch a docker container running a Jupyter notebook server:
```
./launch.sh
```
The first time you run the command, it will download a docker image which may take some time. Otherwise, it will immediately start the docker container and Jupyter notebook server.

### Access the notebook server in your browser
Copy-paste the 127.0.0.0 line with the token into your browser. The line may look like this:
```
http://127.0.0.1:8888/lab?token=cb12e213613c44cfe99e9e7473083588cc6189f901c827e7
```
The notebook server is now shown in your web browser (works fine in a recent Firefox browser).

### Start a new conversation
To start a new conversation, duplicate and rename the sample notebook file. Open the new notebook file by double clicking on the filename. Run the commands in the notebook, one at a time from the top down, using the COMMAND-ENTER keys.   

You can run a specific GPT model version by changing the model name:
```
model="gpt-4-turbo-preview"
```
or
```
model="gpt-4"
```
More model version information is available [here](https://platform.openai.com/docs/models/gpt-4-and-gpt-4-turbops://platform.openai.com/docs/models/gpt-4-and-gpt-4-turbo).  


### Continue the conversation
To continue the conversation, enter additional prompt requests at the bottom of the file. For instance :
```
prompt = f"""
GPT, my follow-up question is: why are Daffodils yellow ?
"""

response = get_completion(prompt)
print(response)
```

### Multiple conversations
To start additional conversations, start a new notebook file as explained above. You can have multiple conversations at a time. Each notebook is a separate cocnversation.

## Next steps

### Learn to write better prompts
There is a free useful course [ChatGPT Prompt Engineering for Developers](https://www.deeplearning.ai/short-courses/chatgpt-prompt-engineering-for-developers/) which teaches how to write better prompts to interact with GPT or other LLMs.

### More information about the OpenAI API platform

[Platform Overview](https://openai.com/product)  
[Documentation for Developers](https://platform.openai.com/docs/overview)  
[API FAQ](https://help.openai.com/en/collections/3675931-api)  

### ChatGPT
Note that [ChatGPT](https://chat.openai.com/) is OpenAI's webchat application built on top of their platform, using mainly GPT v3.5 and v4.
