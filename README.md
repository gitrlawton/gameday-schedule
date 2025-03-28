# Week 2 Day 1: 30 Day DevOps Challenge

## Project: NFL Schedule API Service

This project is an exercise from the 30 Day DevOps Challenge. It demonstrates the creation of a containerized Flask API service that fetches and provides NFL schedule information using the SerpAPI service.

## Project Overview

The project consists of a Flask-based web application that provides NFL schedule information through a REST API endpoint. The application is containerized using Docker for easy deployment and scalability.

## Features

### NFL Schedule API (`app.py`)

- Provides a `/sports` endpoint that returns NFL schedule information
- Fetches real-time schedule data from SerpAPI
- Returns formatted JSON response with game details including:
  - Away and home teams
  - Venue information
  - Date and time of games
- Includes error handling and graceful fallbacks

### Containerization (`Dockerfile`)

- Uses Python 3.9 slim base image for minimal footprint
- Sets up a working directory for the application
- Installs required dependencies from requirements.txt
- Exposes port 8080 for API access
- Configures the application to run on container startup

## AWS Services Used

- Amazon Elastic Container Service (ECS, Fargate): For container orchestration and deployment
- Amazon Elastic Container Registry (ECR): For storing and managing Docker container images
- Amazon Application Load Balancer: For distributing incoming traffic across containers
- Amazon API Gateway: For creating a RESTful API interface that routes requests to the Application Load Balancer endpoint

## Technologies Used

- Python Flask: Web framework for the API
- Docker: Containerization platform
- SerpAPI: Sports data provider
- Requests: HTTP client for API calls
