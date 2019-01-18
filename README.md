# Finding Continents from a Flight Routes Network
## Omar Boujdaria, Franck Dessimoz, Arnaud Duvieusart and Adrien Vandenbroucque

This repository contains the code for the Project of EPFL's Network Tour of Data Science course. The goal of this project is to perform community detection on a network of flight routes, with the goal of identifying the continents.

## Packages required

In order to run the code properly, you will need the following packages:

- NumPy
- Pandas
- NetworkX
- Scikit-Learn
- Matplotlib
- Python-Louvain
- Geopy
- Cartopy

The structure of the files is the following:
- `Project_NTDS.ipynb` is a notebook used when choosing which method was the best, and
- The `.dat` files are the files containing the data for our project

## Data
The datasets we used can be found on https://openflights.org/data.html. We used the files `routes.dat` and `airports.dat`.

The file `routes.data` contains informations about the flight routes, more precisely it contains the following features:

- Airline 	2-letter (IATA) or 3-letter (ICAO) code of the airline.
- Airline ID 	Unique OpenFlights identifier for airline (see Airline).
- Source airport 	3-letter (IATA) or 4-letter (ICAO) code of the source airport.
- Source airport ID 	Unique OpenFlights identifier for source airport (see Airport)
- Destination airport 	3-letter (IATA) or 4-letter (ICAO) code of the destination airport.
- Destination airport ID 	Unique OpenFlights identifier for destination airport (see Airport)
- Codeshare 	"Y" if this flight is a codeshare (that is, not operated by Airline, but another carrier), empty otherwise.
- Stops 	Number of stops on this flight ("0" for direct)
- Equipment 	3-letter codes for plane type(s) generally used on this flight, separated by spaces


The file `airports.dat`contains informations about the airports, more precisely it contains the following features:

- Airport ID 	Unique OpenFlights identifier for this airport.
- Name 	Name of airport. May or may not contain the City name.
- City 	Main city served by airport. May be spelled differently from Name.
- Country 	Country or territory where airport is located. See countries.dat to cross-reference to ISO 3166-1 codes.
- IATA 	3-letter IATA code. Null if not assigned/unknown.
- ICAO 	4-letter ICAO code. Null if not assigned.
- Latitude 	Decimal degrees, usually to six significant digits. Negative is South, positive is North.
- Longitude 	Decimal degrees, usually to six significant digits. Negative is West, positive is East.
- Altitude 	In feet.
- Timezone 	Hours offset from UTC. Fractional hours are expressed as decimals, eg. India is 5.5.
. DST 	Daylight savings time. One of E (Europe), A (US/Canada), S (South America), O (Australia), Z (New Zealand), N (None) or U (Unknown). See also: Help: Time
- Tz database time zone 	Timezone in "tz" (Olson) format, eg. "America/Los_Angeles".
- Type 	Type of the airport. Value "airport" for air terminals, "station" for train stations, "port" for ferry terminals and "unknown" if not known. In airports.csv, only type=airport is included.
- Source 	Source of this data. "OurAirports" for data sourced from OurAirports, "Legacy" for old data not matched to OurAirports (mostly DAFIF), "User" for unverified user contributions. In airports.csv, only source=OurAirports is included.

We also included the cleaned files that we further used in the project, called `routes_clean.dat` and `airports_clean.dat`

## About the notebook

The first part of the notebook is dedicated to preprocessing and cleaning of the graph.

In the second part, the main work of the project is shown, that is first a review of the main propoerties of the graph, followed by some visualization, and the community detection part. In this part, we present different algorithms, and show the resulting communities. We also measure the quality of the partition by measuring modularity and coverage.


