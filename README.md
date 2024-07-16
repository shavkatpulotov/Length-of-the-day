import datetime

def calculate_day_length(date):
    """
    Calculates the length of the day for a given date.
    
    Args:
        date (datetime.date): The date for which to calculate the day length.
    
    Returns:
        datetime.timedelta: The length of the day.
    """
    # Get the sunrise and sunset times for the given date
    sunrise = datetime.datetime.combine(date, datetime.time(6, 0, 0))  # Assuming sunrise at 6:00 AM
    sunset = datetime.datetime.combine(date, datetime.time(18, 0, 0))  # Assuming sunset at 6:00 PM
    
    # Calculate the length of the day
    day_length = sunset - sunrise
    
    return day_length

# Example usage
date = datetime.date(2023, 4, 15)
day_length = calculate_day_length(date)
print(f"The length of the day on {date} is {day_length}.")
Here's how the code works:

The calculate_day_length function takes a datetime.date object as input, representing the date for which you want to calculate the day length.
Inside the function, we create datetime.datetime objects for the sunrise and sunset times on the given date. In this example, we assume the sunrise is at 6:00 AM and the sunset is at 6:00 PM, but you can adjust these values as needed.
We then calculate the day length by subtracting the sunrise time from the sunset time, which gives us a datetime.timedelta object representing the length of the day.
Finally, the function returns the calculated day length.
In the example usage, we create a datetime.date object for April 15, 2023, and pass it to the calculate_day_length function. The resulting day length is then printed to the console.

You can modify the sunrise and sunset times in the code to match your specific location or use more advanced methods to retrieve the actual sunrise and sunset times for a given date and location.
