# Docker Application Deployment

## Step 1: Deploy a Sample Web Application Using Docker

### Install Docker on Your System

1. Download Docker Desktop.
2. Run the installer and follow the instructions.
3. Start Docker Desktop.
4. Verify the installation by running the following command in Command Prompt or PowerShell:
			docker --version

## Step 2: Create a Simple HTML and CSS Web Application

### Create a project directory where your HTML and DockerFile will reside:
	mkdir docker-app
	cd docker-app

### Create an index.html file with the following content:

	<!DOCTYPE html>
	<html lang="en">
	<head>
	    <meta charset="UTF-8">
	    <meta name="viewport" content="width=device-width, initial-scale=1.0">
	    <title>My App</title>
	    <style>
	        body {
	            font-family: Arial, sans-serif;
	            
	            justify-content: center;
	            text-align: center;
	            height: 100vh;
	            margin: 0;
	            background-color: #f4f4f4;
	        }
	        h1 {
	            color: #333;
	        }
	    </style>
	</head>
	<body>
	    <h1>Hello IITJ!</h1>
	    <h3>This is Assignment 1 of VCC - Docker Application Deployment</h3>
	    <h5>Deployed on Docker<br>Aneerban Chowdhury (G23AI2059) - PGDDE @ IITJ</h5>
	</body>
	</html>

## Step 3. Create a Dockerfile

### Create a Dockerfile with the following content:

        FROM nginx:alpine
        COPY index.html /usr/share/nginx/html/index.html
        Build and Run the Docker Image
        Build the Docker image:

### Build the App
        docker build -t myapp

## Step 4: Run the Docker container:
        docker run -p 8080:80 myapp
        
## Step 5: Test the Application
        Navigate to http://localhost:8080

## Author Details
        Roll Number: G23AI2059
        Name: Aneerban Chowdhury
