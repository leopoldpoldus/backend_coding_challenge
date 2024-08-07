# Coding Challenge Case Study: Deforestation Due Diligence Tool

## Objective
Create a backend application using FastAPI that helps companies perform due diligence on deforestation activities by analyzing data from CSV files, performing calculations, returning results, and storing certain results in a database.

## Scenario
You have been hired by a non-profit organization, GreenGuard, that aims to help companies perform due diligence on their supply chains to ensure they are not contributing to deforestation. GreenGuard collects data on deforestation activities, which companies can use to assess the environmental impact of their supply chains. Your task is to create a backend application that can handle these CSV files, perform necessary calculations, return the results, and store some of the insights in a database for future reference.

## Requirements
- **FastAPI**: Use FastAPI to create the backend application.
- **CSV Handling**: Implement functionality to upload and read a CSV file.
- **Data Processing**: Perform specific calculations on the CSV data.
- **Database Interaction**: Save certain results to a database.
- **API Endpoints**: Provide API endpoints to interact with the application.

## Detailed Task Description

### Project Setup
1. Initialize a FastAPI project.
2. Use a virtual environment and specify dependencies in `requirements.txt` (FastAPI, SQLAlchemy, databases, pandas).

### CSV Upload Endpoint
1. Create an endpoint to upload a CSV file.
2. Ensure the CSV file is saved temporarily for processing.

### Data Processing
1. Read the uploaded CSV file using pandas.
2. Perform the following calculations:
   - Calculate the total deforested area (`deforested_area`) reported in the dataset.
   - Find the maximum deforested area for a single event.
3. Return these results in the response.

### Database Interaction
1. Use SQLAlchemy and SQLite (or any other preferred database) for simplicity.
2. Define a table schema to store the results of the calculations.
3. Create an endpoint to save these results into the database.
4. Create another endpoint to retrieve all stored results from the database.

### API Endpoints
- `/upload-csv`: POST endpoint to upload the CSV file.
- `/calculate`: GET endpoint to perform calculations and return results.
- `/save-results`: POST endpoint to save calculation results to the database.
- `/get-results`: GET endpoint to retrieve all stored results from the database.

## Sample CSV Data
```csv
event_id,deforested_area,location,date
1,100.5,Amazon,2024-01-01
2,200.0,Congo,2024-02-15
3,150.75,Amazon,2024-03-10
4,250.25,Indonesia,2024-04-22
5,300.0,Amazon,2024-05-05
```

## Implementation Steps

### Project Structure
```
deforestation_due_diligence_tool/
├── main.py
├── models.py
├── database.py
├── schemas.py
├── requirements.txt
└── .env
```
