# FastAPI Top2

## Project description

This project is a simple FastAPI API that takes a list of phrases and returns the top 2 closest phrases. The API uses the bge embedding model to calculate the text embeddings of the phrases, and the cosine distance ( a metric that measures distances ) to measure the similarity between them. The API can be useful for finding similar phrases or sentences in a corpus of text.

## Project requirements and dependencies

This project requires Python 3.6 or higher and the following packages:

- fastapi
- uvicorn
- requests
- bge

You can install the packages using the following command:

```bash
pip install -r requirements.txt

You can set up and run the project by :

git clone https://github.com/your_username/fastapi-top2.git to clone the repo to your local machine
cd fastapi-top2 to navigate to the project directory
uvicorn main:app --host 0.0.0.0 --port 8000 to run the API server
python demo.py to test the API and the output should be on the form of ('first phrase','second phrase') the closest/similar 2


To make use of the project:
curl -X POST http://0.0.0.0:8000/top2 -H "Content-Type: application/json" -d '{"phrases": ["phrase1", "phrase2", "phrase3"]}'
This command tells the API there is a POST request with JSON ( a type of data format ) payload. And the API should return the top2 closest phrases.
