# OpenAI API Notebook

Here are instructions to start a conversation with GPT in a Jupyter notebook using the OpenAI API. It's only the bare basic of what the OpenAI platform API has to offer. There are links to more information about the OpenAI platform at the bottom of this document.

### Install Docker 
[on MacOS](install_docker_macos.md)  
[on Ubuntu 22.04](install_docker_ubuntu.md)

### Download this repo
From a new terminal
```
git clone git@github.com:versavel/openai-api-notebook.git
```
### Enter your API key
Go the the directory where you installed the repo, for example
```
cd openai-api-notebook
```
And then enter the /jovyan directory
```
cd jovyan
```
Create a file called "key" and enter your API key in the file

### Launch a Jupyter notebook server
Go the the directory where you installed the repo, for example
```
cd openai-api-notebook
```
Open a new terminal window and run the following command:
```
./launch.sh
```
The first time you run the command, it will download a docker image which may take some time. Otherwise, it will immediately start the docker container and Jupyter notebook server.

### Access the notebook server
Copy-paste the 127.0.0.0 line with the token into your browser. The line may look like this:
```
http://127.0.0.1:8888/lab?token=cb12e213613c44cfe99e9e7473083588cc6189f901c827e7
```
The notebook server is now shown in your web browser. 

### Start a new conversation
To start a new conversation, duplicate and rename the sample notebook file. Open the new notebook file by double clicking on the name. Run the commands one at a time using the COMMAND-ENTER keys, from the top down.   

You can run a specific GPT model version by changing the model name:
```
model="gpt-4-turbo-preview"
```
or
```
model="gpt-4"
```
More model version information is available at https://platform.openai.com/docs/models/gpt-4-and-gpt-4-turbops://platform.openai.com/docs/models/gpt-4-and-gpt-4-turbo.  


### To Continue the conversation
To continue the conversation, enter additional prompt requests at the bottom of the file. For instance :
```
prompt = f"""
GPT, my follow-up question is: why are Daffodils yellow ?
"""

response = get_completion(prompt)
print(response)
```

### Multiple conversations
To start a second conversation, start a new notebook file as explained above. You can have multiple conversations at a time. Each notebook is a separate cocnversation.



## More information on OpenAI API platform

[Platform Overview](https://openai.com/product)  
[Documentation for Developers](https://platform.openai.com/overview)  
[API FAQ](https://help.openai.com/en/collections/3675931-api)  

[ChatGPT (v3.5 is free)](https://chat.openai.com/)