# Chatbot Project

This repository contains the code for a simple chatbot using PyTorch and Natural Language Processing (NLP) techniques. The chatbot is designed to respond to user inputs based on predefined intents.

## Table of Contents
- [Installation](#installation)
- [Usage](#usage)
- [Project Structure](#project-structure)
- [Model Architecture](#model-architecture)
- [Training](#training)
- [Running the Chatbot](#running-the-chatbot)
- [Dependencies](#dependencies)
- [License](#license)

## Installation

1. Clone the repository:
    ```bash
    git clone https://github.com/bishaldan/chatbot.git
    cd chatbot
    ```

2. Create and activate a virtual environment (optional but recommended):
    ```bash
    python -m venv venv
    source venv/bin/activate  # On Windows, use `venv\Scripts\activate`
    ```

3. Install the required dependencies:
    ```bash
    pip install -r requirements.txt
    ```

## Usage

1. Prepare the intents JSON file (`intents.json`) with your intents and patterns.
2. Train the model using `train.py`:
    ```bash
    python train.py
    ```
3. Run the chatbot using `chat.py`:
    ```bash
    python chat.py
    ```

## Project Structure

- `chat.py`: Script to run the chatbot.
- `model.py`: Defines the neural network model.
- `nltk_utils.py`: Utility functions for tokenizing and processing text.
- `train.py`: Script to train the chatbot model.
- `intents.json`: JSON file containing intents, patterns, and responses.
- `data.pth`: File to save the trained model state and data.

## Model Architecture

The chatbot model is a simple feedforward neural network with one hidden layer. The architecture is defined in `model.py`.

- Input Layer: Size equals the number of unique stemmed words in the training data.
- Hidden Layer: Configurable size (default is 8).
- Output Layer: Size equals the number of unique tags.

## Training

The training process is handled by `train.py`. The script:
1. Loads and processes the intents data.
2. Creates training data by converting patterns into bag-of-words vectors.
3. Defines the neural network, loss function, and optimizer.
4. Trains the model and saves the trained state to `data.pth`.

## Running the Chatbot

To run the chatbot, execute `chat.py`:
```bash
python chat.py
```
The script will load the trained model, and you can interact with the chatbot in the console.

## Dependencies

- Python 3.6+
- PyTorch
- NLTK

Install the dependencies using:
```bash
pip install -r requirements.txt
```
