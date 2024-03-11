
<div align="center">
  <a href="https://github.com/emanuelebev/Ai-Fitness">
    <img src="img/marketplace.png" alt="Logo" width="200" height="150">
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
* Ensure MongoDB is running and accessible. If you're using MongoDB Atlas or another cloud provider, obtain the URI and store it in AWS SSM Parameter Store under the specified name (/fitnessApp/mongodb_uri).
* Adjust the .env file or set environment variables accordingly to match your MongoDB URI, AWS region, and any other configurations.

## Running the App
To start the app, navigate to the app directory and run:
```
flask run
```
If deployed on an EC2 instance, ensure the security group settings allow inbound HTTP or HTTPS traffic.

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

