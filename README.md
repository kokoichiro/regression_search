# Linear regression best model search tool

This is a documentation to describe supporting code to explore optimal linear regression model and how to deploy it.
***

## Overview of code
This code provides optimal combination of variables for regression model based on business KPI, accuracy on training data and test data.
As final output, this tool provided all the detail about generated model.

### Data Source
* two csv file
	-training data
	-test data

### Technology
* Python
	- pipenv
	- Pandas
	- statsmodel
	- numpy


***
## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes. See deployment for notes on how to deploy the project on a live system.


### Prerequisites
You should download all files from this github
```
git clone git@github.com:kokoichiro/regression_search
```

Using pipenv as version and environment management tool.
If you don't have pipenv, you need to install pipenv.
```
pip install pipenv
```

Download pipfile and locate your working folder.
Put the following commands.
```
pipenv --python 3
pipenv install
pipenv shell
```


## Manual running
You can run the whole processes of this tool with the command below.
```
python XX.py $CONFIGURATION_FILE --mode 'all'
```


### Metrics Description
* measurability:% of impressions which are measurable(publsihers allow us to track viewability)
* viewability: % of impressions which are viewable
* fraud imp: % of impressions which are consumed by non-human traffic or in inappropriate way.
* fraud click: % of clicks which are done by non-human traffic or in inappropriate way.
* inappropriate rate: % of impressions which is delivered to inappropriate contents which is defined by your client/market.You can set your own 'inappropriate contents list' from Google sensitive contents([sensitive content in DV360/DCM]).

## Control
Amnet records all tool usage with Bigquery and [Tracking table] let you know the best parmeter setting from all the past running of IQO.

## Data Definition
Please check the documentation from Google if you need to check the definition of each metric and data.
[verification in DV360/DCM]
[sensitive content in DV360/DCM]



[jupyter notebook]: https://github.com/dan-global/iqo-google/blob/master/IQO%20data%20extraction-dataintegration-20181123.ipynb
[configiration sample file]: https://github.com/dan-global/iqo-google/blob/master/configuration/configuration_sample.yml
[the example of visualisation]: https://datastudio.google.com/reporting/1BUrFFqcXYGmDTO0732BK2eAYy6wsi5xs/page/f0xc
[sensitive content in DV360/DCM]: https://support.google.com/displayvideo/answer/6327207?hl=en
[verification in DV360/DCM]: https://support.google.com/displayvideo/answer/3271318?hl=en&ref_topic=4390839
[Apache Airflow]: https://airflow.apache.org/
[Docker]: https://www.docker.com/
[Tracking table]: https://bigquery.cloud.google.com/table/iprospect-global-data-lake:iqo_manchester_all.iqo_manchester_all?pli=1