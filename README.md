# paco
For Lighspeed Gen AI Hackathon. A guardian for the patient.

# Paco: A Guardian for the Patient

## Table of Contents

1. [Prerequisites](#prerequisites)
2. [Installation](#installation)
3. [Running the Project](#running-the-project)
4. [Troubleshooting](#troubleshooting)
5. [Usage](#usage)
6. [Contributing](#contributing)
7. [License](#license)

## Prerequisites

Before getting started with the Paco project, ensure that you have the following prerequisites:

- Python installed on your system
- Node.js and npm installed on your system
- Basic understanding of command line interface (CLI)

## Installation

### Create a Python Virtual Environment:

```bash
python -m venv venv
```

### Activate the Virtual Environment:

- On Windows:

```bash
venv\Scripts\activate
```

- On Unix or MacOS:

```bash
source venv/bin/activate
```

### Install Python Dependencies:

```bash
pip install -r requirements.txt
```

**Note:** If you're a Windows user, remove the `pyobjc` packages from `requirements.txt` before installing.

### Update ChatGPT API Keys:

Open `LLM.py` and update the API key as follows:

```python
api_key = "type your api key here"

gpt3 = ChatOpenAI(
    # model='gpt-4',
    temperature=0.2,
    streaming=True,
    verbose=True,
    openai_api_key=api_key
)

gpt4 = ChatOpenAI(
    model='gpt-4',
    temperature=0.2,
    streaming=True,
    verbose=True,
    openai_api_key=api_key
)
```

Also, update the API key in `transcribeWhisper.py`:

```python
def process_audio(recognizer, audio, model, fn):
    print("[whisper] Processing audio...")
    text = recognizer.recognize_whisper_api(audio, api_key="paste your api key here")
    print("[whisper] transcript: ", text)
```

### Install Google Text to Speech (if not installed):

```bash
pip install google-text-to-speech
```

## Running the Project

### Backend:

Run the following command:

```bash
python main.py
```

### Frontend:

Navigate to the front-end directory:

```bash
cd front-end
```

Install dependencies:

```bash
npm install
```

If the above command fails, delete the `node_modules` folder and try again.

Start the frontend server:

```bash
npm start
```

## Troubleshooting

If the frontend gives an error "miick not connected", follow these steps:

1. Go to the front-end directory.
2. Open `Env.sample` file and replace the NG Rock link with `http://localhost:5000`.
3. Save the file.
4. Run the frontend again.

## Usage

Click on the start button and start speaking. Enjoy using the project!

## Contributing

Contributions to the Paco project are welcome! If you'd like to contribute, please fork the repository, make your changes, and submit a pull request.

## License

This project is licensed under the [MIT License](LICENSE).

## Ruff

Table of Contents

Prerequisites
Installation
Running the Project
Troubleshooting
Usage
Contributing
License
Prerequisites
Python installed on your system
Node.js and npm installed on your system
Basic understanding of command line interface (CLI)
Installation
Create a Python Virtual Environment:

bash
Copy code
python -m venv venv
Activate the Virtual Environment:

On Windows:

bash
Copy code
venv\Scripts\activate
On Unix or MacOS:

bash
Copy code
source venv/bin/activate
Install Python Dependencies:

bash
Copy code
pip install -r requirements.txt
Note: If you're a Windows user, remove the pyobjc packages from requirements.txt before installing.
Update ChatGPT API Keys:

Open LLM.py and update the API key in the following format:

python
Copy code
api_key="type your api key here"

gpt3 = ChatOpenAI(
    # model='gpt-4',
    temperature=0.2,
    streaming=True,
    verbose=True,
    openai_api_key=api_key
)

gpt4 = ChatOpenAI(
    model='gpt-4',
    temperature=0.2,
    streaming=True,
    verbose=True,
    openai_api_key=api_key
)
Also, update the API key in transcribeWhisper.py:

python
Copy code
def process_audio(recognizer, audio, model, fn):
    print("[whisper] Processing audio...")
    text = recognizer.recognize_whisper_api(audio, api_key="paste your api key here")
    print("[whisper] transcript: ", text)
Install Google Text to Speech (if not installed):

bash
Copy code
pip install google-text-to-speech
Running the Project
Backend:

Run the following command:

bash
Copy code
python main.py
Frontend:

Navigate to the front-end directory:

bash
Copy code
cd front-end
Install dependencies:

bash
Copy code
npm install
If the above command fails, delete the node_modules folder and try again.

Start the frontend server:

bash
Copy code
npm start
Troubleshooting
If the frontend gives an error "miick not connected", follow these steps:
Go to the front-end directory.
Open Env.sample file and replace the NG Rock link with http://localhost:5000.
Save the file.
Run the frontend again.
Usage
Click on the start button and start speaking.
Enjoy using the project!