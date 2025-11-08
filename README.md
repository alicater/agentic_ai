# Ollama Custom GPT Instructions
**What this can do:** 
- read files (.pdf, .docx, .txt) and answer questions about the file.
- answer basic questions 
- ask for clarifying questions
- focuses on student needs

This (as of now) does not have rag implemented, a working memory, or a larger file system working. Only the listed file formats work as of now.

The ides is for this to work similarly to a basic custom gpt like in ChatGPT but locally with Ollama models.

## Run Your Ollama Model
You must start your ollama server and model first, then our python code will connect to that server.

As a reminder to start the server you'll enter the following in your terminal:
```
ollama server
```
*open new terminal*
```
ollama run MODEL_NAME
```
If you want to check which models you have downloaded run ```ollama list``` and if you want more details on a specific model run ```ollama show --modelfile MODEL_NAME```.

## The Code
*Much of this code was generated from ChatGPT and then modified by me to work in more specific ways.*


To begin you'll need to install a few libraries. We'll be working in Python for this but you can do the same thing with javascript as well. I'd suggest making a new virtual environment for this with the below commands in the terminal:

Create the env -
``` python3 -m venv YOUR_PROJECT_NAME ```

Download or copy/paste the 'local_custom_gpt.py' script into this project folder.

Now Activate it -
MacOS/Linux
``` source PROJECT_FOLDER/bin/activate ```
Windows (cmd prompt)
``` PROJECT_FOLDER\Scripts\activate ```
Windoes (powershell)
``` PROJECT_FOLDER\Scripts\activate.ps1 ```

Once you're in the virtual environment install necessay libraries:
``` pip install ollama PyPDF2 docx ```

You should be all good to run the 'local_custom_gpt.py' script. If you want to attach files to your prompt you have to enter `file <pathname>`. You can find the pathname of your file in your file manager (finder, file explorer, etc). Be sure to adjust the model's name to whatever model you're using. I've only been testing with the llama3.1 model which yeilds okay resutls, but a better model would probably be able to yeild even better results. 

