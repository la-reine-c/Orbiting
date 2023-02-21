# Orbital
Combines Celestrak.org with an efficient reverse-gecoder


To use make sure that the folder orbiting is in the same directory as your code

For this to work make sure you have installed ephem, country-converter and pandas. These are modules that are available everywhere. So you can access this via JetBrains. For JetBrains go to Settings > Project: ProjectName Tab > Python Interpreter. The click the plus arrow and type in the name of the modules. You can also access this via Pip.

For example:
    Users/user/Project/orbiting
    Users/user/Project/ActualCode
    
# Imports
    from classes import Satellite, Coordinates
 
# Initializing 
    iss = Satellite(25544) // We do this as it is the Celestrak.org catalog number.
    coord = Coordinates(1.1234, 2.1234) // Latitude goes before longtitude when initializing it. It is the same as writing the pair down.
  
# Get the current lat/long of the satellite
    iss.lat
    iss.long
    
# Get the proper name of the satellite
    iss.name
    
# Get the elsat classificiation of the satellite
    iss.elast_classification
    
# Get the year the satellite launched
    iss.launch_year
    
# Get the current TLE for the satellite
    iss.tle
    
# Get the current elevation of the satellite
    iss.elevation
    
# True if the satellite is currently in the earth's shadow
    iss.is_eclipsed
    
# To get the closest city
    iss.closest_city(accuracy) // Accuracy by default is set to 10. This could take at most 3 seconds depending on the satellites location. Put in a lower accuracy to reduce time. Accuracy can either be a float or int.
    
# To get the closest city of any pair of latitude and longtitude
    coord.closest_city(accuracy) // Accuracy by default is set to 10. This could take at most 3 seconds depending on the satellites location. Put in a lower accuracy to reduce time. Accuracy can either be a float or int.

# Get the difference in km between two latitudes, longtitudes
    coord.distance_between_two_coordinates(lat2, long2) // The lat2 is the latitude of the second pair of coordinates and long2 is the longtitude of the second pair of coordinates.
    
    iss.distance_between_two_coordinates(lat2, long2) // The lat2 is the latitude of the second pair of coordinates and long2 is the longtitude of the second pair of coordinates.
    
    
   
