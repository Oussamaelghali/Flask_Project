# Chatbot Project

## Description

This project involves the development and deployment of an intelligent chatbot capable of interacting with users in natural language. The chatbot leverages Natural Language Processing (NLP) techniques and is trained on a JSON dataset of conversational data. To enhance accessibility, a web interface was created using the Flask framework. Finally, the chatbot was deployed on AWS cloud infrastructure to ensure availability and scalability.

## Features

- **Text Preprocessing**: Tokenization, stemming, and bag-of-words representation for input data.
- **Neural Network Model**: A simple feed-forward neural network trained to classify user intents.
- **Flask Integration**: A web interface for user-friendly interaction with the chatbot.
- **Cloud Deployment**: Hosted on AWS EC2 for global accessibility and scalability.

## Technologies Used

- **Google Colab**: For training the neural network model.
- **PyTorch**: For building and training the neural network.
- **NLTK**: For text preprocessing tasks such as tokenization and stemming.
- **Flask**: For creating a web interface for the chatbot.
- **AWS EC2**: For hosting the chatbot application.

## Project Structure

```
project-directory/
│
├── chatbot.py          # Chatbot implementation and logic
├── model.py            # Neural network model definition
├── nltk_utils.py       # NLP utility functions
├── intents.json        # Training dataset (conversation intents)
├── data.pth            # Saved model parameters
├── app.py              # Flask application
├── templates/
│   └── index.html      # Web interface template
├── static/
│   └── styles.css      # Stylesheet for the web interface
```

## Installation

1. **Clone the repository**:
   ```bash
   git clone <repository-url>
   cd project-directory
   ```

2. **Create a virtual environment**:
   ```bash
   python3 -m venv venv
   source venv/bin/activate
   ```

3. **Install dependencies**:
   ```bash
   pip install -r requirements.txt
   ```

4. **Run the Flask application**:
   ```bash
   flask run
   ```

## Deployment

1. **Prepare AWS EC2 Instance**:
   - Choose an EC2 instance (e.g., `t3.small`).
   - Configure security groups to allow HTTP (port 80) and SSH (port 22).

2. **Set up the server**:
   ```bash
   sudo yum update -y
   sudo yum install python3 python3-pip git
   ```

3. **Clone the project repository**:
   ```bash
   git clone <repository-url>
   cd project-directory
   ```

4. **Install dependencies and set up Gunicorn**:
   ```bash
   python3 -m venv venv
   source venv/bin/activate
   pip install -r requirements.txt
   gunicorn -b 0.0.0.0:8000 app:app
   ```

5. **Configure Nginx**:
   - Update the Nginx configuration file to proxy requests to Gunicorn.

6. **Access the application**:
   - Use the EC2 public IP to access the chatbot.

## Usage

1. Launch the web interface by navigating to the hosted URL.
2. Enter a message in the chatbox and interact with the chatbot.

## Authors

- **Benayad Chakib**
- **El Ghali Oussama**
- **Kouiss Abdessalam**

## Acknowledgements

Special thanks to **Mr. Lahcen Cherif Iyad** for his guidance and support throughout the project.
