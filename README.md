# FastAPI Text Summarization API

This project is a Text Summarization API built using FastAPI. It provides an endpoint to generate summaries for text(url) inputs. 

## Installation

To install the required dependencies, run the following command:

**pip install -r requirements.txt**


This will install the following packages:

- fastapi==0.94.1
- uvicorn==0.21.1
- asyncpg==0.27.0
- tortoise-orm==0.19.3
- aerich==0.7.1
- httpx==0.23.3
- pytest==7.2.2
- gunicorn==20.1.0
- pytest-cov==4.0.0
- flake8==6.0.0
- black==23.1.0
- isort==5.12.0
- pytest-xdist==3.2.1
- newspaper3k==0.2.8

## Usage

To start the API server, use the following command:

**uvicorn main:app --reload**


The API server will start and be accessible at `http://localhost:8000`.

### Endpoints

- `POST /summaries/`: Generates a summary for the provided url. The request body should include the `text` parameter. Example:

curl -X POST -H "Content-Type: application/json" -d '{"url":"https://serengetitech.com/"}' http://localhost:8000/summaries/


- `GET /summaries/{summary_id}/`: Retrieves the summary with the specified `summary_id`. Example:

curl http://localhost:8000/summaries/1/


## Development and Testing

To run the unit tests, use the following command:

pytest --cov=app tests/


## Code Formatting and Linting

We follow certain code formatting and linting standards for this project. To ensure consistency, the following tools are used:

- flake8: For linting the code.
- black: For code formatting.
- isort: For import sorting.

To run the code formatting and linting checks, use the following command:

flake8 .
black .
isort .


Please make sure the code passes these checks before submitting any pull requests or making changes.

## Deployment

This API can be deployed to various platforms or cloud providers. Make sure to configure the deployment settings accordingly. Gunicorn is used as the production server in this project. Additional configurations for deployment can be added in the `gunicorn.conf.py` file.

## License

This project is licensed under the [MIT License](LICENSE). Feel free to modify and use it as per your needs.







