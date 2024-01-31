# Concierge #

## Setup ##

`pip install -r requirements.txt`

copy `.env.example` into a file named `.env` and set the paths to the PDF documents you wish to analyze and a folder on your computer that weaviate will use to store the database.

https://ollama.ai/blog/ollama-is-now-available-as-an-official-docker-image configure the ollama container. The Linux CPU Only instructions seem to work fine on a Windows host too.

## Usage ##

`docker compose up` will start the docker container with the vector DB

`docker exec -it ollama ollama run mistral` will start the docker container with the model

`python loader.py` will load your documents into the database

`python prompter.py` will open the command line interface to query the documents

`python fact-check.py` will open the command line interface to ask true/false questions about the information in the documents

ctrl+C in the docker command-line to stop the container and `docker compose down` to remove
