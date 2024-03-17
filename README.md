
# NLP-Classifier
Introduction
This project trains a Bert model on any NLP classification model. It uses the model to make predictions on new data using batch_inference.py. This architecture can be easily extended to cover a lot more models.

# Installation

Set up
Clone the repository:
git clone https://github.com/Samueoxo/NLP-Classifier.git
cd NLP-Classifier
Move the train.csv and test.csv files to the data folder.

# Python setup:

pip install -r requirements.txt
Copy the training or testing dataset into the "data" folder.

# Run the training script

python training.py
Docker

# Build the Docker image:

docker build -t nlp_classifier .

# Run the Docker container:

docker run -it -v $DATA_FOLDER:/app/data -v $LOCAL_SAVED_MODEL_FOLDER:/app/saved_models nlp_classifier python batch_inference.py
Extra Options

# Managing Configurations
All configurations are in the conf folder, where you can change the data path, model path, etc.

You can also provide the configuration flag while running the script. Use --help after the Python command to see which configs you can change. Example:


python3 batch_inference.py --help
