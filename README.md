# AskNotes in LangFlow

This project allows you to run a flow with a given message and optional tweaks using the LangFlow API. The script `main.py` provides a command-line interface to interact with the flow.

## Prerequisites

- Python 3.6 or higher
- `requests` library
- `python-dotenv` library
- `langflow` library

## Installation

1. Clone the repository:

```sh
git clone https://github.com/TheCarBun/AskNotes-in-LangFlow.git
cd AskNotes-in-LangFlow
```

2. Install the required libraries:

```sh
pip install -r requirements.txt
```

3. Create a `.env` file in the root directory and add your `APPLICATION_TOKEN`:

```env
APPLICATION_TOKEN=your_application_token_here
OPENAI_API_KEY=your_openai_api_key_here
MY_ASTRA_DB_TOKEN=your_astra_db_token_here
```

## Usage

Run the script with the required arguments:

```sh
python main.py "your message here" --endpoint "your_endpoint" --tweaks '{"key": "value"}'
```

### Arguments

- `message` (str): The message to send to the flow.
- `--endpoint` (str): The ID or the endpoint name of the flow. Default is `test`.
- `--tweaks` (str): JSON string representing the tweaks to customize the flow. Default is an empty dictionary.
- `--application_token` (str): Application Token for authentication. Default is the value from the `.env` file.
- `--output_type` (str): The output type. Default is `chat`.
- `--input_type` (str): The input type. Default is `chat`.
- `--upload_file` (str): Path to the file to upload. Default is `None`.
- `--components` (str): Components to upload the file to. Default is `None`.

### Example

```sh
python main.py "Hello, LangFlow!" --endpoint "test" --tweaks '{"OpenAI-XXXXX": {"model_name": "gpt-4"}}'
```

### File Upload

To upload a file, use the `--upload_file` and `--components` arguments:

```sh
python main.py "What do you know?" --upload_file "path/to/your/file.txt" --components "component_name"
```

### Importing the Flow

You can import the flow by importing the `AskNotes.json` file into LangFlow. This file contains the configuration for the flow.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Contributing

Contributions are welcome! Please open an issue or submit a pull request.

## Contact

For any questions or inquiries, please contact [TheCarBun](https://x.com/subhopriyo).
