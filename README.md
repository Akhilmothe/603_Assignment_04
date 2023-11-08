## Tracking the NASA Satellite
![image](https://github.com/Akhilmothe/603_Assignment_04/assets/114513479/8815187c-8cf4-42d5-a102-70479509c642)

1: Introduction
In this code, we are tracking the International Space Station (ISS) using its real-time location data obtained from the "http://api.open-notify.org/iss-now.json" API. We will fetch the ISS's latitude and longitude at regular intervals, plot its location on a map, and save the data to a DataFrame and a CSV file. Additionally, we generate an interactive map in HTML format to visualize the ISS's path over a one-hour period.

Code Explanation:

1. Import Libraries

requests: Used to make HTTP requests to the ISS location API.
time: Used for time-related operations, such as waiting between data fetches.
folium: A Python library for creating interactive maps.
IPython.display: Used to display the generated map in Jupyter Notebook.
pandas: A popular data manipulation and analysis library.
2. Create an Empty DataFrame

We create an empty pandas DataFrame named iss_data_df to store latitude and longitude values.
3. Define a Function fetch_and_plot_iss_location_for_one_hour()

This function fetches the ISS's location data, plots it on a map, and saves the data.
4. Fetch and Plot ISS Location for One Hour

The function fetches data from the ISS API and plots its location on a Folium map for one hour (3600 seconds).
It starts by creating an empty map with specified boundaries and zoom level.
5. Data Fetch Loop

Inside a loop that runs for one hour, the code does the following:
Makes a request to the ISS location API and extracts the latitude and longitude.
Adds a marker on the map with a tooltip displaying the current latitude and longitude.
Connects the current location to the previous location with a blue line.
Appends latitude and longitude values to the data_to_append list.
Sleeps for 5 seconds before fetching the next data.
6. Data Storage

The latitude and longitude data collected during the loop are appended to the iss_data_df DataFrame.
The map is saved as an HTML file named "iss_location_tracking.html."
7. Save Data to CSV

The iss_data_df DataFrame is saved to a CSV file named "iss_location_data.csv."
8. Display the Map

Finally, the generated HTML map is displayed as an iframe in the Jupyter Notebook.
By running this code, you can track the ISS's path for one hour, visualize it on an interactive map, and store the latitude and longitude data in a CSV file for further analysis.





