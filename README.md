# Flask Hello World on Elastic Beanstalk

This is a simple Flask application deployed on **AWS Elastic Beanstalk**.

![Hello World Screenshot](./app_screenshot.png)

## Usage

Visit the Elastic Beanstalk URL to see the app serving a “Hello, World” request.


---

## Table of Contents

- [Requirements](#requirements)  
- [Setup](#setup)  
- [Project Structure](#project-structure)  
- [Creating a Virtual Environment](#creating-a-virtual-environment)  
- [Running Locally](#running-locally)  
- [AWS Elastic Beanstalk Deployment](#aws-elastic-beanstalk-deployment)  

---

## Requirements

- Python 3.10+  
- pip  
- AWS account with access to Elastic Beanstalk  
- AWS CLI installed and configured  
- EB CLI installed  

---

## Setup

1. Clone the repository:

```bash
git clone <your-repo-url>
cd flask-hello-eb

---

## Project Structure 

flask-hello-eb/
│
├── application.py        # Main Flask app
├── requirements.txt      # Python dependencies
├── .elasticbeanstalk/    # Elastic Beanstalk configuration files
├── .github/              # Github Actions
├── buildspec.yml         # AWS CodeBuild for CI/CD
└── README.md             # This file

---

## Creating a Virtual Environment

1. Create and activate a virtual environment:

```bash
python3 -m venv venv
source venv/bin/activate

2. Install dependencies:

```bash
pip install -r requirements.txt

3. Install EB CLI if not installed:
```bash
pip install awsebcli
eb --version

---

## Running Locally

```bash
export FLASK_APP=application.py
export FLASK_ENV=development
flask run

---

## AWS Elastic Beanstalk Deployment

1. Initialize EB environment:

```bash
eb init -p python-3.10 flask-hello-eb

2. Create an environment (example flask-env):

```bash
eb create flask-env

3. Deploy the app:

```bash
eb deploy

4. Open your application in a browser:

```bash 
eb open

