# OpenAI API Notebook

Following are instructions start the Jupyter notebook server in a Docker container and open a Jupyter notebook to run ChatGPT queries.

### Install Docker (MacOS)
1. Download Docker Desktop for Mac
   Visit the Docker website and download Docker Desktop for Mac. You can find it at this URL: https://www.docker.com/products/docker-desktop

2. Install Docker Desktop
   Once the Docker.dmg file is downloaded, double-click on it to open the installer. Then, drag and drop the Docker.app into the Applications folder.

3. Run Docker Desktop
   Navigate to your Applications folder in Finder and double-click on Docker.app to launch it. You may be asked to enter your system password to grant permissions.

4. Verify the Installation
   To verify that Docker has been installed correctly, open a terminal window and type `docker version`. You should see information about the installed Docker version.

5. Start Using Docker
   Now you can start using Docker. You can run a test by typing `docker run hello-world` in the terminal. This command downloads a test image and runs it in a container. When the container runs, it prints an informational message and exits.

Remember, Docker Desktop includes Docker App, developer tools, Kubernetes, and version synchronization between production and development. Docker Desktop automatically updates itself when new versions are available.

### Install Docker on Ubuntu 22.04

### Download this repo
```
git clone git@github.com:versavel/openai-api-notebook.git
```

### Launch a Jupyter notebook server
Go the the directory where you installed the repo, for example
```
cd openai-api-notebook
```
Open a new terminal window and run the following command:
```
./launch.sh
```
The first time you run the command, it will download a docker image. Otherwise, I will start the docker container and Jupyter notebook server.

### Access the notebook server
Copy-paste the 127.0.0.0 line with the token into your browser. The line may look like this:
```
http://127.0.0.1:8888/lab?token=cb12e213613c44cfe99e9e7473083588cc6189f901c827e7
```
The notebook server is now shown in your web browser. Duplicate and rename the sample notebook. Open the new notebook. Run the commands one at a time using the COMMAND-ENTER keys. You can run different models by changing the model name:
```
model="gpt-4"
```
or
```
model="gpt-4-1106-preview"
```
To continue the conversation, enter new prompt requests like :
```
prompt = f"""
Explain why Daffodils are yellow ?
"""

response = get_completion(prompt)
print(response)
```

