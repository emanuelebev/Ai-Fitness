
<div align="center">
  <a href="https://github.com/emanuelebev/Ai-Fitness">
    <img src="static/white-logo.png" alt="Logo" width="200" height="150">
  </a>

<h3 align="center">Fitness Exercise Recommender</h3>

  <p align="center">
    
  </p>
</div>

## Overview
The Fitness Exercise Recommender is a web application designed to help users find exercise recommendations based on their preferences such as primary muscles targeted, fitness level, and equipment available. It utilizes a Flask backend with HTML, JavaScript, and CSS for the frontend, and MongoDB for storing exercise data. Recommendations are powered by a TF-IDF vectorizer and cosine similarity for personalized exercise suggestions. The app is hosted on an AWS EC2 instance, with an IAM role for secure access, and a custom domain configured with DNS to point to the EC2 machine.

## Features
* User-friendly interface to select fitness preferences.
* Personalized exercise recommendations based on user input.
* Detailed instructions and images for each exercise.
* Hosted on AWS for reliable access.

## Installation
**Prerequisites**
* Python 3.6+
* pip
* MongoDB

## Setup
* Clone the repository to your local machine or EC2 instance.
* Install required Python packages:
```
pip install -r requirements.txt
```
* Ensure MongoDB is running and accessible. If you're running the app locally and not using MongoDB Atlas or another cloud provider, you need to:
    - Uncomment the line client = MongoClient("mongodb://localhost:27017/") in the app.
    - Comment out or remove the part of the code that gets the MongoDB client from AWS secrets.
* For cloud-based MongoDB or to store MongoDB URI in AWS SSM Parameter Store, ensure the AWS CLI is configured with the necessary permissions.

## Running the App Locally
To start the app locally, ensure MongoDB is running on your local machine. Then, navigate to the app directory and run:
```
python app.py
```

## Deployment on AWS EC2 with SSL
The current web application is hosted on an EC2 instance. To deploy your application in a similar environment, you will need:
* An AWS EC2 instance set up for hosting your Flask application.
* A domain name configured with DNS to point to your EC2 instance.
* Nginx installed on your EC2 instance to serve your Flask application and to configure SSL for HTTPS access.
* Obtain an SSL certificate for your domain, for example, through Let's Encrypt.
* Configure Nginx to use the SSL certificate, enabling HTTPS for your web application.
* Ensure the security group for your EC2 instance allows inbound HTTP (port 80) and HTTPS (port 443) traffic.

## Usage
Navigate to the app's URL (local or deployed) in a web browser. You'll be presented with options to choose your fitness level (beginner or advanced) and preferences such as primary muscles to target and equipment. After submitting your preferences, the app will recommend exercises matching your criteria.

## Contributing
Contributions are welcome! If you'd like to improve the Fitness Exercise Recommender, please follow these steps:

* Fork the repository.
* Create a new branch (git checkout -b feature/AmazingFeature).
* Make your changes.
* Commit your changes (git commit -m 'Add some AmazingFeature').
* Push to the branch (git push origin feature/AmazingFeature).
* Open a pull request.

## Acknowledgments
* MongoDB for database services.
* AWS for cloud hosting and services.
* Flask for the backend framework.
* Pandas and Scikit-learn for data processing and recommendations.

