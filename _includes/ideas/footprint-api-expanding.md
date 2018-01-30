
## Carbon Footprint - API

### Idea: Expansion of CO2 Emissions API

#### Description

Carbon footprint API is a 2017 GSoC Project, which is currently robust enough to calculate dependent and independent carbon emission from the sources. At present we are dependent on the very small data set which is used directly to calculate carbon emission for different endpoints.

We are planning to have a machine learning based backend API which will contain models and will be connected to existing API. This basically involves finding suitable real-world datasets based on carbon emission API and using the same to train machine learning models. These models will be hooked up to a python based web server maybe Flask or tornado and allow the rest API to query specific emission rates.

**Note - You are supposed to propose the datasets in your GSoC proposal or beforehand.**


Project url [here](https://gitlab.com/aossie/CarbonFootprint-API),
project is live at [https://carbonhub.xyz](https://carbonhub.xyz)

#### Requirements

For this project, we are looking for a student with:

- motivation to search, find and understand sources of reliable scientific data about CO2 emissions.

- OOP, Python, Tornado (primarily for its web-socket functionality) or Flask framework, Scikit-Learn, Basic understanding of Machine Learning.



#### Mentors

Bruno Woltzenlogel Paleo, Chirag Arora, Kolya Opahle, Prateek Gupta, Saisankar Gochhayat, Vaibhav Sharma, Nakul Havelia. 
