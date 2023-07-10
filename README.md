# Event Weather and Flight API

This project is a Python Django API that provides information about events, weather, and flights. It consumes external 3rd party APIs to list events in a country, retrieve the current weather at the event location, and provide a list of flights to attend those events based on the user's airport code.

**Note: This project was developed as part of an interview application for PwC.**

---

## Installation

To run this project locally, follow these steps:

1. Clone the repository:
git clone git@github.com:Sara-Alkhateeb/Assignment-PWCevent.git

arduino
Copy code

2. Create a virtual environment: 
python -m venv venv

markdown
Copy code

3. Activate the virtual environment.

4. Install the required dependencies:
pip install -r requirements.txt

markdown
Copy code

5. Apply the database migrations:
python manage.py migrate

yaml
Copy code

## Usage

To use the API, follow these steps:

1. Start the Django development server:
python manage.py runserver

markdown
Copy code

2. Access the API endpoints using a tool like cURL, Postman, or any HTTP client of your choice.

- To retrieve a list of events in a specific country, make a GET request to `http://localhost:8000/events/` with the `country` parameter set to the desired country code.

- To get the current weather for a specific event, make a GET request to `http://localhost:8000/weather/` with the `id` parameter set to the desired event ID.

- To get a list of flights for a specific event and airport, make a GET request to `http://localhost:8000/flights/` with the `event_id` and `airport_code` parameters set to the desired values.

3. Inspect the responses from the API to obtain the requested information.

## API Endpoints

- `events/`
- Description: Retrieve a list of events in a specific country.
- Method: GET
- Parameters:
 - country: The country code (e.g., "US", "GB").
- Response: JSON object containing a list of events.

- `weather/`
- Description: Retrieve weather information for a specific event.
- Method: GET
- Parameters:
 - id: The ID of the event.
- Response: JSON object containing weather information.

- `flights/`
- Description: Retrieve a list of flights for a specific event and airport.
- Method: GET
- Parameters:
 - event_id: The ID of the event.
 - airport_code: The airport code.
- Response: JSON object containing a list of flights.

## Technologies Used

The project utilizes the following technologies and libraries:

- Python
- Django
- SQLite
- Django REST Framework
- Requests (for making HTTP requests to 3rd party APIs)

---

## License

This project is licensed under the MIT License.

Feel free to modify and adapt this project according to your needs.
