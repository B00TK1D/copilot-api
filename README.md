# Copilot.api

Provides a simple HTTP API to interface with GitHub Copilot, including native GitHub authentication.

## Installing dependencies

`pip install -r requirements.txt`

## Run
`python3 api.py [port]`

## Usage
Send a POST request to `http://localhost:8080/api` with the following JSON body:

### Request payload
```json
{
    "prompt": "# hello world function\n\n",
    "language": "python"
}
```

### Response

The response will be a plain text string containing the generated code.

```text
def hello_world():
```

In order to build a complete code snippet, iteratively append the generated code to the prompt and send it back to the API until the response is empty.
