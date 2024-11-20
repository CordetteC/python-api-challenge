Module 6 was completed with the help of Xpert Learning Assistant and Instructor office hours.

WeatherPy
from datetime import datetime
Get today's date
today_date = datetime.now().strftime("%Y-%m-%d")

VacationPy
map_plot = city_data_df.hvplot.points(
    x='longitude', 
    y='latitude', 
    geo=True, 
    size='humidity', 
    color='City',  # You can use a column for color if desired
    tiles='OSM',   # Using OpenStreetMap as the tile source
    frame_width=800,  # Set the width of the frame
    frame_height=600  # Set the height of the frame
)

Add an empty column, "Hotel Name," to the DataFrame so you can store the hotel found using the Geoapify API
hotel_df['Hotel Name'] = None

Add the current city's latitude and longitude to the params dictionary
    params["filter"] = f"circle:{longitude},{latitude},{radius}"  # Filter for a specific location
    params["bias"] = f"point:{longitude},{latitude}"  # Bias the search towards the hotel's location
