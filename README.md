# Satu's testing onprem.LLM demo

Using https://github.com/arska/onpremllm as a starting point, which uses https://github.com/amaiya/onprem with a modified frontend to demo different models and RAG as a starting point.

## Installation

- On Linux, skip this, but utilise on mac: Macbook pro M1 with Mac Os 14 (Sonoma), I used Python 3.11 (3.12 did not work), installed from MacPorts (https://www.macports.org/install.php)
- create a virtual environment to install in: python3 -m virtualenv venv; source venv/bin/activate
- Install llama-cpp-python on linux without added arguments and with a mac utilise Apple Metal support: CMAKE_ARGS="-DLLAMA_METAL=on" FORCE_CMAKE=1 pip install llama-cpp-python
- Install the other dependencies: pip install -r requirements.txt

## Running

- load the python environment: source venv/bin/activate
- start the WebGUI: streamlit run app.py

## Data

- onprem stores all models and vectordb at "~/onprem_data/"
- we use the (supplied) PDF in ./sample_data/ for retrieval augmented generation (RAG)

## Screenshot

![Screenshot](screenshot.png)
