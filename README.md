## API Documentation

The API documentation is automatically generated using Swagger and can be accessed at the following URL:

[Swagger UI](https://<your-render-app-url>/apidocs/)

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
