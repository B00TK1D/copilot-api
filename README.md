# Copilot.api

Provides a simple HTTP API to interface with GitHub Copilot, including native GitHub authentication.

## Installing dependencies

`pip install -r requirements.txt`

## Run
`python3 api.py [port]`

## Usage
Send a POST request to `http://localhost:8080/api` with the following JSON body:
```json
{
    "system_message": "You are a helpful assistant.",
    "user_message": "Could you please help me create a Python script that takes a list of numbers as input and returns a list of those numbers sorted in ascending order? The script should handle both positive and negative numbers and should ignore any non-numeric values in the input list"
}
```

## Response
The response will be a plain text string containing the generated code.

In order to build a complete code snippet, iteratively append the generated code to the prompt and send it back to the API until the response is empty.
