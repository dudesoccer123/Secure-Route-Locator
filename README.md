# Secure-Route-Locator
identifies the nearest shelter location to the user providing them with essential data regarding route, distance to target location, estimated time of arrival etc helping save lives in event of emergencies like natural disasters

## Project Features:
 * Interactive Map with details of the nearest safe locations.
 * Automatically takes the user’s current location without requiring user intervention.
 * Calculation of best route and expected time of arrival. 
 * Hyperlinks to websites containing emergency numbers for quick access.

## Technologies Used: 

Backend: 
* Majorly implemented using the Python programming language.
* OpenRouteService API for route generation between 2 coordinates.
* Geopy Library for geocoding and reverse geocoding.
* Folium library for map generation.

Frontend:
* built a website using React JS and the backend of the website using Node JS communicating with the Python file.

## Role: 
Served as backend developer in the project, contributing to geocoding, calculating distance between the coordinates, identifying the route with the shortest distance, generating route using an API call and interactive map creation.


## Usage Guide

1. **Obtaining Coordinates:**
    - Get the coordinates for your starting location, for example, from Google Maps. Replace these coordinates in the `start_coords` variable in the code.
    ```python
    start_coords = (latitude, longitude)[::-1]  # Replace latitude and longitude
    ```

2. **Defining Safe House Coordinates:**
    - Define coordinates for safe houses near your starting location. Replace these coordinates in the `safe_house_coords` list in the code.
    ```python
    safe_house_coords = [
        [safe_house1_latitude, safe_house1_longitude][::-1],
        [safe_house2_latitude, safe_house2_longitude][::-1],
        # Add more safe house coordinates as needed
    ]
    ```

3. **OpenRouteService API Key:**
    - Create an account on OpenRouteService and obtain an API key. Replace `'api key'` with your API key in the code.
    ```python
    api_key = 'your_openrouteservice_api_key'
    ```

4. **Running the Code:**
    - Once you've replaced the necessary variables, run the code. The map will be displayed with markers for the starting location and safe houses, along with the shortest route to the nearest safe house.

5. **Interpreting Results:**
    - After running the code, the console will display statistics such as total distance, estimated time of arrival, and the area name of the nearest safe house. These results will also be saved in a text file named `data.txt`.


