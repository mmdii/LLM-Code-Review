# LLAMA-Code-Reviewer

Example usage

``` bash
python maincode.py --api=http://382e-34-143-193-144.ngrok.io /path/to/your/repo/folder
```

# How it works

LLAMA-Code-Reviewer runs on it's own process and waits for file changes. As it gets new file changes it will generate code reviews using the Colab API you run. It will keep a queue of the past 10 files that have been reviewed.

LLAMA-Code-Reviewer currently using a flask api running from a Google Colab to prompt Code Llama.

# How to use it

### Set up the Google Colab

Go to the peresentation directory and copy colab file in you google colab then run the server and copy the ngrok url

You have to run all the cells and ensure the flask server is running properly

### Clone the repo

``` bash

git clone git@github.com:mmdii/LLM-Code-Review.git
cd LLAMA-Code-Review
```

### Install the packages

``` bash
pip install -r requirements.txt
```

The arguments/options

``` bash
usage: maincode.py [-h] [--api API] repository

positional arguments:
  repository  Pass in the source code folder you want to watch

options:
  -h, --help  show this help message and exit
  --api API   Link to the colab ngrok url
```

### Run it

Example command

``` bash
python maincode.py --api=http://382e-34-143-193-144.ngrok.io /path/to/your/repo/folder

```