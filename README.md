# `US-Domestic-Airline-Flights-Performance`
## `Objective` :
As Data Analyst , We are given a task to monitor and report the US Domestics Airline Flights Performance . The main goal of this Project is to Analyze the performance of reporting Airline to improve the flight reliability thereby imporoving customers reliability

Below are the key reporting Items :
* Yearly Airline Performance Repprt
* Yearly Average Flight Delay Statistics

## `Components of the Dashboard Report`
### 1. Yearly Airline Performance Repprt
* Number of Flights under different cancellation cateogory using `Bar Chart`
* Average flights time by reporting airline using `Line chart`
* Percentage of diverted airport landings per reprting airline using `Pie chart`
* Number of flights flying from each state using `Choropleth Map`
* Number of flights flying to each state from a reporting airline using `treemap chart`
### 2. Yearly Average Flight Delay Statistics
* Monthly average `Carrier delay` by reporting airline for the givven year
* Monthly average `Weather delay` by reporting airline for the givven year
* Monthly average `Ntional Air System delay` by reporting airline for the given year.
* Monthly average `Security delay` by reporting airline for the given year.
* Monthly average `Late Aircraft delay` by reporting airline for the given year.
## `What I had Done`
## Task 1 : Imported Packages
* `Pandas`
* `dash`
* `plotly`
* `plotly.graph_objects as go`
* `plotly.express as px`
* `dash_html_components as html`
* `dash_core_components as dcc`
* `dash.dependencies`
## Task 2 : Added Title to the Dashboard
* Provided the title of the application as `US Domestic Airline Flights Performance` using `html.H1()`
* Made the heading center aligned, set color as `#503D36`, and font size as `24`.
## Task 3 : Added the Dropdown menu
* Created two dropdown menues for selceting the report type and year using `dcc.Dropdown()`
* Set `id` as `input-type` to be a parameter.
* Set `options` to list containing dictionaries with key as `label` and user provided value for labels in `value`.

  1st dictionary

  * label: Yearly Airline Performance Report
  * value: OPT1
    
  2nd dictionary

  * label: Yearly Airline Delay Report
  * value: OPT2
    
* Set placeholder to `Select a report type`.

* Set width as `80%`, padding as `3px`, font size as `20px`, text-align-last as `center` inside style parameter dictionary.
## Task 4 : Added a division with two empty divisions inside
* Add a division with two empty divisions inside
* Provide division `ids` as `plot4` and `plot5`. Display style as `flex`.
## Task 5 : Added 5 ouput components
* It is a list with 5 output parameters with component id and property. Here, the component property will be `children` as we have created empty division and passing in `dcc.Graph`
* Component `ids` will be `plot1` , `plot2`, `plot2`, `plot4`, and `plot5`.
## Task 6 : Average flight time by reporting airline
* Created a line plot using returned dataframe `line_data` from the above function `compute_data_choice` using `plotly.express`.
* Set:

  * Figure name as `line_fig`
  * Input data as `line_data`
  * x as `Month`, y as `AirTime`, color as `Reporting_Airline` and title as `Average monthly flight time (minutes) by airline`.
