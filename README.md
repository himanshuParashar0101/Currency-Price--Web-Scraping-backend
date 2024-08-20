# Vanced Backend-Himanshu Parashar

## Prerequisites
-Python installed on your machine.
-Required Python packages specified in `requirements.txt`.

## Installation
-Clone the Repository:

    git clone https://github.com/himanshuParashar0101/vance-backend.git
    cd vance-backend
- Run the following command to install all the necessary dependencies:

 `pip install -r requirements.txt`\
 
 Running the Application\
 Run the Cron Script:\
 `cron_script.py`
#### Before starting the API, run the cron script to keep the data synced with `Yahoo Finance`:
### Start the API Server:

After running the cron script, start the API server:
`python api.py`\
The backend will run on `http://localhost:5000`.

Additional Notes
Make sure that both the cron script and the API server are running to keep the data in sync and the backend functional.\
The backend API endpoints are designed to provide historic forex data to the frontend.
## API Documentation

The API documentation is automatically generated using Swagger and can be accessed at the following URL:

[Swagger UI](https://vance-backend.onrender.com/apidocs/#/)

### Endpoint

- **POST /api/forex_data**

  Retrieves historical forex data based on the provided query parameters.

  **Query Parameters:**
  - `from`: The currency code to convert from (e.g., USD).
  - `to`: The currency code to convert to (e.g., INR).
  - `period`: The time period to retrieve data for (e.g., 1W, 1M, 3M, 6M, 1Y).

  **Responses:**
  - `200`: Returns the forex data in JSON format.
  - `400`: Missing required parameters or invalid period.
  - `404`: No data found for the given parameters.
  - `500`: Failed to retrieve data.
