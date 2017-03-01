
## Carbon Footprint

### Idea: CO2 Emissions API

#### Description

Carbon Footprint is currently a browser extension (for Chrome, Firefox and Safari) that calculates CO2 emissions incurred when driving (or using public transportation) on routes suggested by map services such as Google Maps, Here and Open Street Map. To do that, we implemented functions (in Javascript) that convert distance, time, fuel type and other inputs into CO2. These functions are potentially useful for other projects as well, but they are currently not accesible outside Carbon Footprint. We would like to transform these useful functions into two APIs:

1. A javascript API consisting of a single and well-documented Javascript file that could be imported by other projects. (This is expected to be easy and just a matter of refactoring code that we already have.)
2. A RESTful web API that would allow clients to submit GET requests containing inputs such as distance, time and fuel type and obtain the corresponding CO2 emissions as response in JSON.

Furthermore, we would like to expand the set of CO2 conversion functions that we already have as much as possible. We would like our APIs to be able to calculate the CO2 footprint of *everything*, and not only driving and public transportation. For instance, we would like to have: a function that takes a given amount of electricity (in kWh) and the country where it was generated, and outputs the CO2 emissions incurred in generating it; a function that takes a given plant species and an amount of time and outputs how much CO2 the plant will absorb in that amount of time; a function that takes an amount and type of meat, and how much CO2 was released in producing it; a function that takes an animal species and an amount of time and outputs how much CO2 it creates while breathing; and so on... We want a universal converter to CO2.

The conversion functions should be implemented using reliable scientific data.

If you apply for this idea, please give some details about how you would implement  and host the RESTful API. And please list which conversion functions you would implement (preferably citing/linking the sources you would use).

#### Requirements

For this project, we are looking for a student:

- with basic knowledge of Javascript, HTML, CSS and RESTful web services.

- motivation to search, find and understand sources of reliable scientific data about CO2 emissions.



#### Mentors

Chirag Arora, Kolya Opahle, Prateek Gupta, Bruno Woltzenlogel Paleo




