## **Module 3: Introduction to Data Science**

---

### **1. Data Science Workflow**
#### **Theory (Brief)**:  
- **What is Data Science?**  
  - Overview and importance in solving real-world problems (e.g., healthcare, finance, e-commerce).
  - Understanding the role of a **data scientist** and the data science lifecycle.
- **Data Science Workflow** covers everything from **data collection** to **data transformation** before any modeling. This is a crucial step as it prepares the data for further analysis.

#### **Practical Tasks**:
1. **Data Collection**:  
   - **Task**: Fetch data from real-world sources:
     - **APIs**: Pull data from a public API (e.g., **OpenWeather API** for weather data).
     - **Web Scraping**: Use **BeautifulSoup** and **Requests** to scrape real-time product data from an e-commerce site.
     - **Databases**: Connect to a **MySQL** database, query it using **SQLAlchemy**, and load data into **Pandas** DataFrame.
     - **File I/O**: Load data from CSV, Excel, or JSON files using **Pandas**.

2. **Data Cleaning**:  
   - **Task**: Clean a dataset (e.g., **Titanic Dataset** or **Customer Data**).
     - **Missing Values**: Handle missing values using **mean/median imputation** for numerical data and **mode imputation** for categorical columns.
     - **Duplicates**: Remove duplicate rows from the dataset using **Pandas** `.drop_duplicates()`.
     - **Outliers**: Detect and handle outliers using **box plots** or **Z-scores**.
     - **Practical Scenario**: You have sales data with missing values and outliers, and you need to clean it to ensure accurate analysis.

3. **Data Transformation**:  
   - **Task**: Perform essential data transformations for machine learning readiness.
     - **Feature Engineering**: Create new features (e.g., **Total Revenue** from **Quantity** * **Price**).
     - **Scaling & Normalization**: Scale numerical features using **MinMaxScaler** or **StandardScaler** from **Scikit-learn**.
     - **Categorical Encoding**: Convert categorical variables into numerical format using **One-Hot Encoding** or **Label Encoding**.


### **2. Exploratory Data Analysis (EDA)**
#### **Theory (Brief)**:  
- **EDA** helps to explore and understand the data, identify trends, detect outliers, and draw insights from the dataset before applying any modeling techniques.

#### **Practical Tasks**:
1. **Descriptive Statistics**:
   - **Task**: Calculate key summary statistics for a dataset (e.g., **Iris dataset** or **Sales dataset**) using **Pandas**.
     - Mean, Median, Mode: Central tendencies of the dataset.
     - **Variance & Standard Deviation**: Measure the spread of data.
     - **Skewness and Kurtosis**: Identify the shape of the data distribution.
     - **Practical Scenario**: Calculate the average purchase price and variability in **Sales dataset** to understand customer spending behavior.

2. **Data Visualization**:
   - **Task**: Visualize various aspects of the data to gain insights:
     - **Box Plots**: Identify data distribution and outliers (use **Seaborn**).
     - **Histograms**: Understand the frequency distribution of features (e.g., sales per customer).
     - **Scatter Plots**: Visualize relationships between two numerical features (e.g., **Age vs. Income** for customer segmentation).
     - **Pair Plots**: Explore relationships between multiple continuous variables (e.g., explore how **Age**, **Income**, and **Spending** are related).
     - **Heatmaps**: Display correlation matrices to analyze feature relationships.

3. **Correlation**:
   - **Task**: Use **Pandas** and **Seaborn** to create correlation matrices for a dataset (e.g., analyzing how **age**, **income**, and **purchasing frequency** relate).
     - Create and interpret **heatmaps** to visually identify correlations.
     - **Practical Scenario**: You want to see how various factors (age, education, income) affect customer spending in a retail dataset.

4. **Interactive Visualizations**:  
   - **Task**: Create interactive dashboards using **Plotly**.
     - **Scatter Plots**: Create interactive **scatter plots** to visualize the relationship between two variables.
     - **Bar Charts**: Build interactive bar charts to show the frequency of categorical data.



### **3. Tools for Data Science (Libraries & Functions)**
#### **Pandas**:
   - **Key Functions**: `.read_csv()`, `.drop()`, `.fillna()`, `.groupby()`, `.pivot_table()`.
   - **Practical Task**: Load a **real-world dataset**, perform cleaning (e.g., remove duplicates), and preprocess the data (e.g., fill missing values).

#### **NumPy**:
   - **Key Functions**: `np.array()`, `np.mean()`, `np.std()`, `np.nanmean()`.
   - **Practical Task**: Use **NumPy** for basic numerical operations like calculating **mean**, **standard deviation**, and handling **NaN values**.

#### **Matplotlib & Seaborn**:
   - **Matplotlib**: Basic plotting (e.g., line, bar, scatter, and histograms).
   - **Seaborn**: Advanced visualizations like **box plots**, **pair plots**, **heatmaps**, and **regression plots**.
   - **Practical Task**: Visualize the relationship between **customer age** and **spending** in a dataset using **Seaborn** pair plots.

#### **Plotly**:
   - **Key Functions**: `plotly.express.scatter()`, `plotly.express.line()`, `plotly.express.bar()`.
   - **Practical Task**: Build an interactive **scatter plot** for the **Iris dataset** using **Plotly**. Implement a hover feature to show details of each data point.



### **4. Garbage Collection and Data Restructuring**  
#### **Practical Tasks**:
1. **Memory Optimization**:
   - **Theory (Brief)**: **Garbage collection** in Python helps optimize memory when handling large datasets.
   - **Practical Task**: Use **gc.collect()** to clear unused objects from memory.
   - **Practical Scenario**: Clean up a **large dataset** to prevent memory overflow while performing data transformations.

2. **Reshaping Data**:
   - **Practical Task**: Use **Pandas** functions like `.melt()`, `.pivot()`, and `.stack()` to restructure the dataset from wide to long format for specific tasks.
   - **Practical Scenario**: Restructure a **sales dataset** to show each product’s sale as a row (from wide format to long format) for analysis.




---


### **What is Data?**

#### **1. Introduction to Data**
- **Definition of Data:**
  - *Data* is raw information that can exist in many forms — **numbers**, **text**, **images**, **videos**, etc. However, data itself is **meaningless** until we analyze it.

- **Real-World Example:**  
  - **Temperature Readings:** A city's temperature readings are collected. These numbers are data, but until analyzed, this data doesn’t provide useful insight.

- **Role of Data in Daily Life:**
  - **Smartphones:** All the apps running on your phone are based on **data**. For example, Facebook, Instagram — these apps track your activity, what posts you like, which friends you interact with, all of this is **data**.

#### **2. Data’s Journey:**
- **From Raw Data to Meaningful Insights:**
  - **Real-World Example:**  
    - A **retail store’s** data — such as sales, inventory, and customer demographics — is raw data. By **analyzing** it, the store can figure out which products are selling well and which customer segments to target.
  
- **Torturing the Data to Extract Insights:**
  - **Case Study:**  
    - **Netflix**’s recommendation system: Netflix "tortures" the data to suggest shows you’ve already watched or shows that align with your interests. This is done using a **complex algorithm** based on the data that matches your preferences.

#### **3. Importance of Data Today:**
- **Data as the New Oil:**
  - In today’s world, data is called the **“new oil”**. Data is a resource that, if used correctly, can make any **business** extremely **powerful**. If you have more **data**, you can predict market trends, optimize your products, and maximize your sales.

---

### **What is Science?**

#### **1. Introduction to Science:**
- **Definition of Science:**
  - *Science* is a systematic method in which we gather **facts**, create **hypotheses**, and then draw **conclusions** through experiments or analysis.

- **Real-World Example:**
  - **Physics:** Understanding Newton's **laws of motion** is a scientific approach. You observe, then conduct experiments to draw conclusions.

#### **2. The Role of Science in Data:**
- **Scientific Approach to Data:**  
  When we analyze **data** scientifically, we organize our **observations** systematically, then create models to help us understand the data.

- **Real-World Case Study:**
  - **Climate Change Studies:** Scientists analyzed **global temperature data** to predict how temperatures may increase over the next decades. This analysis helps policymakers implement **environmental policies**.

---

### **Combining Data + Science = Data Science**

#### **1. What is Data Science?**
- **Definition of Data Science:**  
  When we process **data** scientifically and extract **meaningful insights** from it, this process is called **Data Science**.

- **Real-World Example:**
  - **Healthcare:** **Predictive models** that analyze a patient’s health to predict risk factors and recommend proper treatment — all done through **Data Science**.

#### **2. The Data Science Workflow:**
- **Step 1: Data Collection:**  
  - **Example:** Facebook collects user activity data, like what posts you interact with, where you click, and how much time you spend on the platform.
  
- **Step 2: Data Cleaning:**  
  - **Real-World Example:** If an **e-commerce website** has customer review data, but some reviews are incomplete or have typos, they need to be cleaned to make the data accurate.
  
- **Step 3: Data Transformation:**  
  - **Example:** Retail stores need to transform sales data into formats that can be used to predict trends. This transformation makes the analysis easier.

- **Step 4: Data Analysis & Modeling:**  
  - **Real-World Example:**  
    - **Financial Sector:** A bank uses customer transaction data to predict which customers might default on loans. **Predictive modeling** helps them flag risky clients early.

#### **3. Data Science in Real Life:**
- **How Data Science Affects Us Daily:**  
  - **Example:** Online shopping platforms like **Amazon** use **Data Science** to recommend products based on your previous searches and buying habits. 

- **Data Science in Business:**  
  - **Example:** **Walmart** uses data science to predict which products will be in demand during peak seasons, helping them optimize inventory and distribution.

#### **4. The Power of Data: How Data can Make a Country a King or Slave**
- **Data in Economics:**  
  - **Example:** Countries like **USA** and **China** leverage massive amounts of **data** for their **economic growth**. They collect data on trade, manufacturing, and consumer behavior to stay ahead in the global market.
  
- **Data as a Source of Power:**  
  - Countries with **better data management systems** can make better **decisions** in terms of **policy-making, economy**, and even **geopolitics**. For example, **China** uses data to manage its **supply chains** efficiently, making it a **global economic powerhouse**.

#### **5. Real-World Case Study: The Role of Data Science in Modern Economics**
- **Case Study – China’s Economic Strategy Through Data:**
  - China has utilized data in a **big way**. They track everything from **population density, resource utilization**, to **economic growth** using data science. This has allowed them to become a **global leader in manufacturing** and **technology**.

---

### **Data Science Workflow: A Crucial Step in the Data Science Process**

The **Data Science Workflow** covers all the key stages from **data collection** to **data transformation** before any modeling begins. These steps are essential in ensuring that the data is prepared correctly for further analysis and predictive modeling. Let's break down each phase:

#### **1. Data Collection**
   - **What Happens Here?**  
     The first step in any data science project is **collecting data**. This can come from various sources such as surveys, sensors, APIs, and internal business databases.
   - **Real-World Example:**  
     A **weather forecasting system** collects data from satellites, sensors, and weather stations to predict weather patterns.

#### **2. Data Cleaning**
   - **What Happens Here?**  
     Raw data is often incomplete, inconsistent, or inaccurate. **Data cleaning** involves removing errors, duplicates, and missing values to ensure the dataset is accurate and reliable.
   - **Real-World Example:**  
     An **e-commerce company** may have sales data with missing product details or customer information. Cleaning the data will make sure there are no missing values that could cause misinterpretation during analysis.

#### **3. Data Transformation**
   - **What Happens Here?**  
     Data is often transformed into a format that is suitable for analysis. This could include **normalization**, **aggregation**, or **encoding** data into categorical variables.
   - **Real-World Example:**  
     A **bank** might aggregate transaction data by **month** to analyze spending patterns over time. Similarly, categorical data like "High," "Medium," and "Low" spending may need to be converted into numerical values (1, 2, 3) for modeling.

#### **4. Data Modeling (Next Step after Transformation)**
   - **What Happens Here?**  
     Once the data has been properly collected, cleaned, and transformed, the next step involves building **models** (such as regression, classification, or clustering models) to gain insights and make predictions.
   - **Real-World Example:**  
     A **healthcare system** might use predictive modeling to forecast patient readmissions based on past medical records and patient history.

---


### **Data Science Lifecycle: A Step-by-Step Process**

The **Data Science Lifecycle** is a structured process that guides data scientists through every phase of a data science project. It covers everything from **understanding the problem** to **communicating the results**. Below are the key stages of the lifecycle:

#### **1. Problem Understanding & Business Objective**
   - **What Happens Here?**  
     The first step is understanding the **business problem** or the **question** that needs to be answered. This step involves **interacting with stakeholders** to understand the goal of the analysis.
   - **Real-World Example:**  
     A **retail company** wants to understand why certain products are not selling well. The business objective is to improve sales by identifying which factors are affecting product sales.
   - **Key Questions:**
     - What problem are we trying to solve?
     - What is the objective of the analysis?
     - Who are the stakeholders?

#### **2. Data Collection**
   - **What Happens Here?**  
     Once the problem is understood, the next step is to **collect relevant data**. This data can come from various sources, such as internal databases, APIs, external datasets, surveys, and sensors.
   - **Real-World Example:**  
     A **financial institution** may collect data from their customer transaction records, credit scores, and loan histories to predict the likelihood of loan defaults.

#### **3. Data Cleaning & Preparation**
   - **What Happens Here?**  
     Raw data often contains errors, inconsistencies, missing values, or irrelevant information. **Data cleaning** and **preparation** ensure that the dataset is free from anomalies and ready for analysis.
   - **Real-World Example:**  
     A **social media platform** may collect user data, but this data might include **duplicate entries**, **missing location information**, or **incorrect timestamps**. Cleaning ensures that only valid and relevant data is used.
   - **Steps Involved:**
     - Removing duplicates
     - Handling missing values
     - Correcting data types

#### **4. Exploratory Data Analysis (EDA)**
   - **What Happens Here?**  
     **Exploratory Data Analysis (EDA)** involves visually and statistically exploring the data to **identify patterns, trends, and relationships** within the data.
   - **Real-World Example:**  
     A **marketing team** at a company may analyze customer demographic data to see if there are any patterns in **age, location, and purchasing behavior**.
   - **Tools Used:**
     - **Matplotlib**, **Seaborn** for data visualization
     - **Pandas** for statistical summaries
     - **Histograms, Box plots, Scatter plots** for uncovering trends

#### **5. Data Transformation**
   - **What Happens Here?**  
     Data transformation is the process of converting data into a format that is suitable for analysis and modeling. This step can include **normalizing, aggregating**, and **encoding** data.
   - **Real-World Example:**  
     A **bank** might convert **categorical data** (like "High," "Medium," "Low" credit score) into **numeric data** to use in a machine learning model.
   - **Transformation Tasks:**
     - Feature scaling (Normalization/Standardization)
     - Encoding categorical variables
     - Creating new features based on existing data (e.g., combining date and time)

#### **6. Data Modeling**
   - **What Happens Here?**  
     Once the data is prepared, the next step is to build **predictive models** using various algorithms like **regression**, **classification**, or **clustering**. This step involves selecting the right model, training it, and fine-tuning parameters.
   - **Real-World Example:**  
     A **healthcare provider** may use a **logistic regression model** to predict whether a patient will be readmitted to the hospital based on their medical history and demographics.
   - **Common Algorithms:**
     - **Linear Regression** for predictions
     - **Decision Trees** for classification
     - **K-Means Clustering** for segmenting customers

#### **7. Model Evaluation**
   - **What Happens Here?**  
     After building the model, it is important to evaluate its performance using various **metrics** to ensure it’s accurate and useful. This can involve **cross-validation**, testing on unseen data, and checking for overfitting.
   - **Real-World Example:**  
     A **bank** may evaluate a **credit risk model** by checking the **accuracy, precision, recall**, and **F1 score** to make sure the model correctly identifies high-risk customers.
   - **Evaluation Metrics:**
     - **Accuracy, Precision, Recall, F1-Score**
     - **Confusion Matrix**
     - **ROC Curve**

#### **8. Model Deployment**
   - **What Happens Here?**  
     After a successful evaluation, the model is **deployed** to the real-world environment where it can be used to make predictions on new data.
   - **Real-World Example:**  
     **Spotify** deploys its music recommendation system to provide users with personalized playlists. The deployed model continuously learns and improves based on user interactions.
   - **Deployment Tools:**
     - **APIs** to expose the model
     - **Cloud platforms** like AWS, Azure, or Google Cloud for hosting

#### **9. Monitoring & Maintenance**
   - **What Happens Here?**  
     Post-deployment, the model is **monitored** to ensure it continues to perform well as new data comes in. Over time, the model may need to be **retrained** or **updated**.
   - **Real-World Example:**  
     **Amazon** regularly updates its recommendation engine to reflect new products and user preferences, ensuring the recommendations stay relevant.
   - **Maintenance Tasks:**
     - Tracking model performance over time
     - Retraining the model with new data
     - Adjusting model parameters as needed



### **1. Data Collection**

Data collection is the first step in any data science project, where we gather data from different sources like **APIs**, **web scraping**, **databases**, or **files** (CSV, JSON, etc.). Let's go through each of these techniques with examples.

---

#### **1.1. Fetching Data from an API (OpenWeatherAPI)**

**Real-World Scenario:**  
We’ll fetch **weather data** for Karachi from the **OpenWeatherAPI**. This is a common task for getting real-time data such as weather forecasts or market prices.



```python
import requests
import pandas as pd

# API URL and Key
API_KEY = "bed36b0ce19142bbb8873238251504"
city = "Karachi"
url = f"http://api.weatherapi.com/v1/current.json?key={API_KEY}&q={city}"

# Send GET request to the API
response = requests.get(url)

# Parse the response as JSON
weather_data = response.json()

# Normalize the JSON data to create a structured DataFrame
weather_df = pd.json_normalize(weather_data)

# Print the first few rows of the data
print(weather_df.head())
```

      location.name location.region location.country  location.lat  location.lon  \
    0       Karachi           Sindh         Pakistan       24.8667         67.05   
    
      location.tz_id  location.localtime_epoch location.localtime  \
    0   Asia/Karachi                1744879769   2025-04-17 13:49   
    
       current.last_updated_epoch current.last_updated  ...  current.windchill_f  \
    0                  1744879500     2025-04-17 13:45  ...                 87.8   
    
       current.heatindex_c  current.heatindex_f current.dewpoint_c  \
    0                 35.1                 95.2               22.4   
    
      current.dewpoint_f  current.vis_km  current.vis_miles  current.uv  \
    0               72.3             4.0                2.0        10.5   
    
       current.gust_mph current.gust_kph  
    0              25.2             40.6  
    
    [1 rows x 39 columns]
    


```python
# simple technique
# Fetching Data from WeatherAPI.com (JSON)
# First, let's use your provided **WeatherAPI.com** to fetch weather data.

import requests
import pandas as pd
from pprint import pprint

# API URL and Key
url = "http://api.weatherapi.com/v1/current.json"
api_key = "bed36b0ce19142bbb8873238251504"
city = "Karachi"

# Fetch data from the API
response = requests.get(f"{url}?key={api_key}&q={city}")
weather_data = response.json()

pprint(weather_data)
# Convert JSON data into a Pandas DataFrame
# weather_df = pd.json_normalize(weather_data)
# print(weather_df.head())

```

    {'current': {'cloud': 0,
                 'condition': {'code': 1030,
                               'icon': '//cdn.weatherapi.com/weather/64x64/day/143.png',
                               'text': 'Mist'},
                 'dewpoint_c': 20.7,
                 'dewpoint_f': 69.2,
                 'feelslike_c': 42.7,
                 'feelslike_f': 108.8,
                 'gust_kph': 29.4,
                 'gust_mph': 18.3,
                 'heatindex_c': 34.2,
                 'heatindex_f': 93.6,
                 'humidity': 47,
                 'is_day': 1,
                 'last_updated': '2025-04-24 11:30',
                 'last_updated_epoch': 1745476200,
                 'precip_in': 0.0,
                 'precip_mm': 0.0,
                 'pressure_in': 29.74,
                 'pressure_mb': 1007.0,
                 'temp_c': 35.1,
                 'temp_f': 95.2,
                 'uv': 9.3,
                 'vis_km': 4.0,
                 'vis_miles': 2.0,
                 'wind_degree': 264,
                 'wind_dir': 'W',
                 'wind_kph': 25.6,
                 'wind_mph': 15.9,
                 'windchill_c': 31.3,
                 'windchill_f': 88.3},
     'location': {'country': 'Pakistan',
                  'lat': 24.8667,
                  'localtime': '2025-04-24 11:43',
                  'localtime_epoch': 1745476980,
                  'lon': 67.05,
                  'name': 'Karachi',
                  'region': 'Sindh',
                  'tz_id': 'Asia/Karachi'}}
    


```python
import requests
import pandas as pd
import time 
from cachetools import cached, TTLCache 

# cachetools is a Python library used to cache function results, preventing repeated calculations for the same inputs. 
# It helps speed up programs by storing function outputs and reusing them if the same function is called again with the same parameters.
# TTLCache: A specific type of cache that stores values for a certain amount of time (TTL – Time-to-Live). 
# After the TTL expires, the cached value is discarded.
# @cached: A decorator that automatically stores the result of a function in the cache.

# use case: If you're making multiple API calls for the same data (like weather data), 
# caching helps avoid repeated requests within a short period, reducing load times and unnecessary API calls.

# Set up cache with a TTL (Time-To-Live) to store weather data
# TTLCache will store up to 100 items, and each cached item will expire after 600 seconds (10 minutes)

start_time = time.time()  # Track the time it takes to fetch data

cache = TTLCache(maxsize=100, ttl=600)

# Define a function that fetches weather data for a given city, with caching
@cached(cache)  # This decorator caches the result of this function
def fetch_weather_data(city):
    # Create the API request URL using the city name
    url = f"http://api.weatherapi.com/v1/current.json?key=bed36b0ce19142bbb8873238251504&q={city}"
    # Make a GET request to the WeatherAPI to get current weather data for the city
    response = requests.get(url)
    # Return the response in JSON format (which is parsed and used later)
    return response.json()

# List of cities for which we want to fetch weather data
cities = ["Karachi", "Lahore", "Islamabad"]

# Initialize an empty list to store the weather data for each city
weather_data = []

# Loop through the list of cities and fetch their weather data
for city in cities:
    # Call the fetch_weather_data function for each city and store the result in the weather_data list
    data = fetch_weather_data(city)
    weather_data.append(data)  # Add the fetched data for the city to the list

# Convert the list of weather data into a pandas DataFrame for better analysis
# pd.json_normalize is used to flatten nested JSON data into a tabular format


end_time = time.time()  # Track the time after fetching data

# Calculate the time taken to fetch data for all cities
print(f"Time taken to fetch weather data for all cities: {end_time - start_time} seconds")

weather_df = pd.json_normalize(weather_data)

# (Optional) Print the first few rows of the DataFrame to verify the data
# print(weather_df.head())

# Return the DataFrame containing the weather data for all cities
weather_df

```

    Time taken to fetch weather data for all cities: 1.0102527141571045 seconds
    




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>location.name</th>
      <th>location.region</th>
      <th>location.country</th>
      <th>location.lat</th>
      <th>location.lon</th>
      <th>location.tz_id</th>
      <th>location.localtime_epoch</th>
      <th>location.localtime</th>
      <th>current.last_updated_epoch</th>
      <th>current.last_updated</th>
      <th>...</th>
      <th>current.windchill_f</th>
      <th>current.heatindex_c</th>
      <th>current.heatindex_f</th>
      <th>current.dewpoint_c</th>
      <th>current.dewpoint_f</th>
      <th>current.vis_km</th>
      <th>current.vis_miles</th>
      <th>current.uv</th>
      <th>current.gust_mph</th>
      <th>current.gust_kph</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Karachi</td>
      <td>Sindh</td>
      <td>Pakistan</td>
      <td>24.8667</td>
      <td>67.0500</td>
      <td>Asia/Karachi</td>
      <td>1745476980</td>
      <td>2025-04-24 11:43</td>
      <td>1745476200</td>
      <td>2025-04-24 11:30</td>
      <td>...</td>
      <td>88.3</td>
      <td>34.2</td>
      <td>93.6</td>
      <td>20.7</td>
      <td>69.2</td>
      <td>4.0</td>
      <td>2.0</td>
      <td>9.3</td>
      <td>18.3</td>
      <td>29.4</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Lahore</td>
      <td>Punjab</td>
      <td>Pakistan</td>
      <td>31.5497</td>
      <td>74.3436</td>
      <td>Asia/Karachi</td>
      <td>1745477546</td>
      <td>2025-04-24 11:52</td>
      <td>1745477100</td>
      <td>2025-04-24 11:45</td>
      <td>...</td>
      <td>101.3</td>
      <td>37.8</td>
      <td>100.0</td>
      <td>-6.0</td>
      <td>21.2</td>
      <td>6.0</td>
      <td>3.0</td>
      <td>7.9</td>
      <td>6.4</td>
      <td>10.4</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Islamabad</td>
      <td>Islamabad</td>
      <td>Pakistan</td>
      <td>33.7000</td>
      <td>73.1667</td>
      <td>Asia/Karachi</td>
      <td>1745477546</td>
      <td>2025-04-24 11:52</td>
      <td>1745477100</td>
      <td>2025-04-24 11:45</td>
      <td>...</td>
      <td>92.8</td>
      <td>31.7</td>
      <td>89.1</td>
      <td>-1.6</td>
      <td>29.2</td>
      <td>10.0</td>
      <td>6.0</td>
      <td>7.9</td>
      <td>7.0</td>
      <td>11.2</td>
    </tr>
  </tbody>
</table>
<p>3 rows × 39 columns</p>
</div>




```python
import requests
import pandas as pd
import time

# Define a function that fetches weather data for a given city
def fetch_weather_data(city):
    # Create the API request URL using the city name
    url = f"http://api.weatherapi.com/v1/current.json?key=bed36b0ce19142bbb8873238251504&q={city}"
    # Make a GET request to the WeatherAPI to get current weather data for the city
    response = requests.get(url)
    # Return the response in JSON format (which is parsed and used later)
    return response.json()

# List of cities for which we want to fetch weather data
cities = ["Karachi", "Lahore", "Islamabad"]

# Initialize an empty list to store the weather data for each city
weather_data = []

# Loop through the list of cities and fetch their weather data
start_time = time.time()  # Track the time it takes to fetch data

for city in cities:
    # Call the fetch_weather_data function for each city and store the result in the weather_data list
    data = fetch_weather_data(city)
    weather_data.append(data)  # Add the fetched data for the city to the list

end_time = time.time()  # Track the time after fetching data

# Calculate the time taken to fetch data for all cities
print(f"Time taken to fetch weather data for all cities: {end_time - start_time} seconds")

# Convert the list of weather data into a pandas DataFrame for better analysis
# pd.json_normalize is used to flatten nested JSON data into a tabular format
weather_df = pd.json_normalize(weather_data)

# (Optional) Print the first few rows of the DataFrame to verify the data
print(weather_df.head())

# Return the DataFrame containing the weather data for all cities
# weather_df

```

    Time taken to fetch weather data for all cities: 0.7512924671173096 seconds
      location.name location.region location.country  location.lat  location.lon  \
    0       Karachi           Sindh         Pakistan       24.8667       67.0500   
    1        Lahore          Punjab         Pakistan       31.5497       74.3436   
    2     Islamabad       Islamabad         Pakistan       33.7000       73.1667   
    
      location.tz_id  location.localtime_epoch location.localtime  \
    0   Asia/Karachi                1745476980   2025-04-24 11:43   
    1   Asia/Karachi                1745477546   2025-04-24 11:52   
    2   Asia/Karachi                1745477546   2025-04-24 11:52   
    
       current.last_updated_epoch current.last_updated  ...  current.windchill_f  \
    0                  1745476200     2025-04-24 11:30  ...                 88.3   
    1                  1745477100     2025-04-24 11:45  ...                101.3   
    2                  1745477100     2025-04-24 11:45  ...                 92.8   
    
       current.heatindex_c  current.heatindex_f current.dewpoint_c  \
    0                 34.2                 93.6               20.7   
    1                 37.8                100.0               -6.0   
    2                 31.7                 89.1               -1.6   
    
      current.dewpoint_f  current.vis_km  current.vis_miles  current.uv  \
    0               69.2             4.0                2.0         9.3   
    1               21.2             6.0                3.0         7.9   
    2               29.2            10.0                6.0         7.9   
    
       current.gust_mph current.gust_kph  
    0              18.3             29.4  
    1               6.4             10.4  
    2               7.0             11.2  
    
    [3 rows x 39 columns]
    



**Explanation:**
- We use the **requests** library to fetch data from the **OpenWeatherAPI**.
- **`.json()`** extracts the JSON data returned by the API, and **`pd.json_normalize()`** converts it into a **Pandas DataFrame**, which makes it easy to analyze.

---

#### **1.2. Web Scraping (BeautifulSoup)**

**Real-World Scenario:**  
Web scraping is used to **extract real-time data** from websites. For instance, if you need product prices from an e-commerce site, web scraping helps you gather this data automatically.



```python
import requests
from bs4 import BeautifulSoup

# URL to scrape data from
url = 'http://books.toscrape.com/'

# Send GET request to fetch the page
response = requests.get(url)

# Parse the page content using BeautifulSoup
soup = BeautifulSoup(response.content, 'html.parser')

# Find all books on the page
books = soup.find_all('article', class_='product_pod')
# print(book)
# Loop through each book and extract the title and price
book_data = []

for book in books:
    name = book.h3.a['title']
    price = book.find('p', class_='price_color').text
    book_data.append([name, price])

# print(book_data)
# Convert the list of data into a DataFrame
book_df = pd.DataFrame(book_data, columns=['Book Name', 'Price'])

# Show the first few rows
# print(book_df.head())

book_df
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Book Name</th>
      <th>Price</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>A Light in the Attic</td>
      <td>£51.77</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Tipping the Velvet</td>
      <td>£53.74</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Soumission</td>
      <td>£50.10</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Sharp Objects</td>
      <td>£47.82</td>
    </tr>
    <tr>
      <th>4</th>
      <td>Sapiens: A Brief History of Humankind</td>
      <td>£54.23</td>
    </tr>
    <tr>
      <th>5</th>
      <td>The Requiem Red</td>
      <td>£22.65</td>
    </tr>
    <tr>
      <th>6</th>
      <td>The Dirty Little Secrets of Getting Your Dream...</td>
      <td>£33.34</td>
    </tr>
    <tr>
      <th>7</th>
      <td>The Coming Woman: A Novel Based on the Life of...</td>
      <td>£17.93</td>
    </tr>
    <tr>
      <th>8</th>
      <td>The Boys in the Boat: Nine Americans and Their...</td>
      <td>£22.60</td>
    </tr>
    <tr>
      <th>9</th>
      <td>The Black Maria</td>
      <td>£52.15</td>
    </tr>
    <tr>
      <th>10</th>
      <td>Starving Hearts (Triangular Trade Trilogy, #1)</td>
      <td>£13.99</td>
    </tr>
    <tr>
      <th>11</th>
      <td>Shakespeare's Sonnets</td>
      <td>£20.66</td>
    </tr>
    <tr>
      <th>12</th>
      <td>Set Me Free</td>
      <td>£17.46</td>
    </tr>
    <tr>
      <th>13</th>
      <td>Scott Pilgrim's Precious Little Life (Scott Pi...</td>
      <td>£52.29</td>
    </tr>
    <tr>
      <th>14</th>
      <td>Rip it Up and Start Again</td>
      <td>£35.02</td>
    </tr>
    <tr>
      <th>15</th>
      <td>Our Band Could Be Your Life: Scenes from the A...</td>
      <td>£57.25</td>
    </tr>
    <tr>
      <th>16</th>
      <td>Olio</td>
      <td>£23.88</td>
    </tr>
    <tr>
      <th>17</th>
      <td>Mesaerion: The Best Science Fiction Stories 18...</td>
      <td>£37.59</td>
    </tr>
    <tr>
      <th>18</th>
      <td>Libertarianism for Beginners</td>
      <td>£51.33</td>
    </tr>
    <tr>
      <th>19</th>
      <td>It's Only the Himalayas</td>
      <td>£45.17</td>
    </tr>
  </tbody>
</table>
</div>




**Explanation:**
- We use **BeautifulSoup** to parse HTML and extract data from the webpage. 
- The **find_all()** method helps in extracting all the books' names and prices on the page.

---

#### **1.3. Fetching Data from CSV Files (COVID-19 Data)**

**Real-World Scenario:**  
CSV files are commonly used to store **structured data** like **COVID-19** statistics. Let’s load a **CSV file** containing global COVID-19 data into **Pandas**.




```python
import pandas as pd

# URL of the COVID-19 global dataset
url = "https://raw.githubusercontent.com/CSSEGISandData/COVID-19/master/csse_covid_19_data/csse_covid_19_time_series/time_series_covid19_confirmed_global.csv"

# Load the CSV file into a Pandas DataFrame
covid_data = pd.read_csv(url)

# Show the first few rows of the dataset
print(covid_data.head())
```

      Province/State Country/Region       Lat       Long  1/22/20  1/23/20  \
    0            NaN    Afghanistan  33.93911  67.709953        0        0   
    1            NaN        Albania  41.15330  20.168300        0        0   
    2            NaN        Algeria  28.03390   1.659600        0        0   
    3            NaN        Andorra  42.50630   1.521800        0        0   
    4            NaN         Angola -11.20270  17.873900        0        0   
    
       1/24/20  1/25/20  1/26/20  1/27/20  ...  2/28/23  3/1/23  3/2/23  3/3/23  \
    0        0        0        0        0  ...   209322  209340  209358  209362   
    1        0        0        0        0  ...   334391  334408  334408  334427   
    2        0        0        0        0  ...   271441  271448  271463  271469   
    3        0        0        0        0  ...    47866   47875   47875   47875   
    4        0        0        0        0  ...   105255  105277  105277  105277   
    
       3/4/23  3/5/23  3/6/23  3/7/23  3/8/23  3/9/23  
    0  209369  209390  209406  209436  209451  209451  
    1  334427  334427  334427  334427  334443  334457  
    2  271469  271477  271477  271490  271494  271496  
    3   47875   47875   47875   47875   47890   47890  
    4  105277  105277  105277  105277  105288  105288  
    
    [5 rows x 1147 columns]
    

**Explanation:**
- **Pandas** provides an easy way to load **CSV files** from URLs directly into a **DataFrame**. This is the standard method for **handling tabular data**.

---

#### **1.4. Fetching Data from MySQL Database (SQLAlchemy)**

**Real-World Scenario:**  
If you have a **database** that stores business data (e.g., sales data), you can fetch it using **SQLAlchemy** to query and load it into **Pandas**.



```python
import pandas as pd
import sqlalchemy

# Create a connection to the database
engine = sqlalchemy.create_engine('mysql+pymysql://root:admin@localhost/world')

# Write a SQL query to fetch the data
query = "SELECT * FROM city"

# Load the data into a Pandas DataFrame
sales_data = pd.read_sql(query, engine)

# Show the first few rows of the data
print(sales_data.head())
```

       ID            Name CountryCode       District  Population
    0   1           Kabul         AFG          Kabol     1780000
    1   2        Qandahar         AFG       Qandahar      237500
    2   3           Herat         AFG          Herat      186800
    3   4  Mazar-e-Sharif         AFG          Balkh      127800
    4   5       Amsterdam         NLD  Noord-Holland      731200
    


**Explanation:**
- **SQLAlchemy** is used to establish a **connection** to the **MySQL database**.
- The **SQL query** is written to fetch data from the **sales_data** table.

---

### **2. Data Cleaning**
**Theory (Brief):**  
Data cleaning involves handling **missing values**, **duplicates**, and **outliers**. It ensures that the data is **accurate**, **consistent**, and **ready** for analysis or modeling.

**or**

Data cleaning is about making the data **accurate** and **complete** by handling **missing values**, **duplicates**, and **outliers**. Let’s go step by step.

---

#### **2.1. Handling Missing Values**

**Real-World Scenario:**  
In real-world datasets, many columns might have missing values. For example, the **Age** column in the **Titanic dataset** may have missing values. We can fill those missing values using **mean**, **median**, or **mode**.

##### **Program 1: Impute Missing Numerical Data with Median**
We will handle missing values by **imputing** them with the **mean** value of the column.



```python
# import pandas as pd

# # Load Titanic dataset
# # url = "https://web.stanford.edu/class/archive/cs/cs109/cs109.1166/stuff/titanic.csv"
# url = "https://raw.githubusercontent.com/pandas-dev/pandas/master/doc/data/titanic.csv"

# titanic_data = pd.read_csv(url)

# # Impute missing 'Age' values with the mean
# titanic_data['Age'].fillna(titanic_data['Age'].mean(), inplace=True)

# # Display the first few rows of the dataset after imputation
# print(titanic_data.head())


# # # Impute missing 'Age' values with the median
# titanic_data['Age'].fillna(titanic_data['Age'].median(), inplace=True)
# print(titanic_data.head())


import pandas as pd

# Load Titanic dataset
url = "https://raw.githubusercontent.com/pandas-dev/pandas/master/doc/data/titanic.csv"
titanic_data = pd.read_csv(url)


# Impute missing 'Age' values with the mean
# titanic_data['Age'] = titanic_data['Age'].fillna(titanic_data['Age'].mean())
# print("After filling Age with mean:")
# # print(titanic_data.head())
# titanic_data


# Impute missing 'Age' values with the median (if needed again)
# (This is just for demonstration — not usually applied after mean imputation.)
titanic_data['Age'] = titanic_data['Age'].fillna(titanic_data['Age'].median())
print("After filling Age with median:")
# print(titanic_data.head())
titanic_data['Age']
```

    After filling Age with median:
    




    0      22.0
    1      38.0
    2      26.0
    3      35.0
    4      35.0
           ... 
    886    27.0
    887    19.0
    888    28.0
    889    26.0
    890    32.0
    Name: Age, Length: 891, dtype: float64




```python
import pandas as pd

# Load Titanic dataset
url = "https://raw.githubusercontent.com/pandas-dev/pandas/master/doc/data/titanic.csv"
titanic_data = pd.read_csv(url)
titanic_data
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>PassengerId</th>
      <th>Survived</th>
      <th>Pclass</th>
      <th>Name</th>
      <th>Sex</th>
      <th>Age</th>
      <th>SibSp</th>
      <th>Parch</th>
      <th>Ticket</th>
      <th>Fare</th>
      <th>Cabin</th>
      <th>Embarked</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>1</td>
      <td>0</td>
      <td>3</td>
      <td>Braund, Mr. Owen Harris</td>
      <td>male</td>
      <td>22.0</td>
      <td>1</td>
      <td>0</td>
      <td>A/5 21171</td>
      <td>7.2500</td>
      <td>NaN</td>
      <td>S</td>
    </tr>
    <tr>
      <th>1</th>
      <td>2</td>
      <td>1</td>
      <td>1</td>
      <td>Cumings, Mrs. John Bradley (Florence Briggs Th...</td>
      <td>female</td>
      <td>38.0</td>
      <td>1</td>
      <td>0</td>
      <td>PC 17599</td>
      <td>71.2833</td>
      <td>C85</td>
      <td>C</td>
    </tr>
    <tr>
      <th>2</th>
      <td>3</td>
      <td>1</td>
      <td>3</td>
      <td>Heikkinen, Miss Laina</td>
      <td>female</td>
      <td>26.0</td>
      <td>0</td>
      <td>0</td>
      <td>STON/O2. 3101282</td>
      <td>7.9250</td>
      <td>NaN</td>
      <td>S</td>
    </tr>
    <tr>
      <th>3</th>
      <td>4</td>
      <td>1</td>
      <td>1</td>
      <td>Futrelle, Mrs. Jacques Heath (Lily May Peel)</td>
      <td>female</td>
      <td>35.0</td>
      <td>1</td>
      <td>0</td>
      <td>113803</td>
      <td>53.1000</td>
      <td>C123</td>
      <td>S</td>
    </tr>
    <tr>
      <th>4</th>
      <td>5</td>
      <td>0</td>
      <td>3</td>
      <td>Allen, Mr. William Henry</td>
      <td>male</td>
      <td>35.0</td>
      <td>0</td>
      <td>0</td>
      <td>373450</td>
      <td>8.0500</td>
      <td>NaN</td>
      <td>S</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>886</th>
      <td>887</td>
      <td>0</td>
      <td>2</td>
      <td>Montvila, Rev. Juozas</td>
      <td>male</td>
      <td>27.0</td>
      <td>0</td>
      <td>0</td>
      <td>211536</td>
      <td>13.0000</td>
      <td>NaN</td>
      <td>S</td>
    </tr>
    <tr>
      <th>887</th>
      <td>888</td>
      <td>1</td>
      <td>1</td>
      <td>Graham, Miss Margaret Edith</td>
      <td>female</td>
      <td>19.0</td>
      <td>0</td>
      <td>0</td>
      <td>112053</td>
      <td>30.0000</td>
      <td>B42</td>
      <td>S</td>
    </tr>
    <tr>
      <th>888</th>
      <td>889</td>
      <td>0</td>
      <td>3</td>
      <td>Johnston, Miss Catherine Helen "Carrie"</td>
      <td>female</td>
      <td>NaN</td>
      <td>1</td>
      <td>2</td>
      <td>W./C. 6607</td>
      <td>23.4500</td>
      <td>NaN</td>
      <td>S</td>
    </tr>
    <tr>
      <th>889</th>
      <td>890</td>
      <td>1</td>
      <td>1</td>
      <td>Behr, Mr. Karl Howell</td>
      <td>male</td>
      <td>26.0</td>
      <td>0</td>
      <td>0</td>
      <td>111369</td>
      <td>30.0000</td>
      <td>C148</td>
      <td>C</td>
    </tr>
    <tr>
      <th>890</th>
      <td>891</td>
      <td>0</td>
      <td>3</td>
      <td>Dooley, Mr. Patrick</td>
      <td>male</td>
      <td>32.0</td>
      <td>0</td>
      <td>0</td>
      <td>370376</td>
      <td>7.7500</td>
      <td>NaN</td>
      <td>Q</td>
    </tr>
  </tbody>
</table>
<p>891 rows × 12 columns</p>
</div>



**Explanation:**
- **`fillna()`** is used to replace missing values in the **'Age'** column with the **mean** of that column.

##### **Program 2: Impute Missing Data with Mode (Categorical)**

For **categorical columns**, we will impute missing values with the **mode** (most frequent category).



```python
import pandas as pd

url = "https://raw.githubusercontent.com/pandas-dev/pandas/master/doc/data/titanic.csv"

titanic_data = pd.read_csv(url)

# It fills the missing 'Embarked' values with the mode (most frequent value),
# which helps preserve the distribution of categorical data without removing rows.

# Impute missing 'Embarked' values with the mode (most frequent value)
titanic_data['Embarked'] = titanic_data['Embarked'].fillna(titanic_data['Embarked'].mode()[0])

# titanic_data['Embarked'].fillna(titanic_data['Embarked'].mode()[0], inplace=True)


# Display the first few rows of the dataset after imputation
# print(titanic_data.head())
titanic_data['Embarked']


```




    0      S
    1      C
    2      S
    3      S
    4      S
          ..
    886    S
    887    S
    888    S
    889    C
    890    Q
    Name: Embarked, Length: 891, dtype: object



**Explanation:**
- We use the **mode** to fill missing values in the **'Embarked'** column, which is categorical.

##### **Program 3: Remove Duplicates**

Sometimes, data contains duplicate rows that need to be removed.



```python
import pandas as pd

url = "https://raw.githubusercontent.com/pandas-dev/pandas/master/doc/data/titanic.csv"

titanic_data = pd.read_csv(url)

# Remove duplicate rows from the Titanic dataset
titanic_data.drop_duplicates(inplace=True)

# Display the first few rows of the dataset after removing duplicates
print(titanic_data.head())

```

       PassengerId  Survived  Pclass  \
    0            1         0       3   
    1            2         1       1   
    2            3         1       3   
    3            4         1       1   
    4            5         0       3   
    
                                                    Name     Sex   Age  SibSp  \
    0                            Braund, Mr. Owen Harris    male  22.0      1   
    1  Cumings, Mrs. John Bradley (Florence Briggs Th...  female  38.0      1   
    2                              Heikkinen, Miss Laina  female  26.0      0   
    3       Futrelle, Mrs. Jacques Heath (Lily May Peel)  female  35.0      1   
    4                           Allen, Mr. William Henry    male  35.0      0   
    
       Parch            Ticket     Fare Cabin Embarked  
    0      0         A/5 21171   7.2500   NaN        S  
    1      0          PC 17599  71.2833   C85        C  
    2      0  STON/O2. 3101282   7.9250   NaN        S  
    3      0            113803  53.1000  C123        S  
    4      0            373450   8.0500   NaN        S  
    


**Explanation:**
- **`.drop_duplicates()`** is used to remove exact duplicate rows from the dataset.

##### **Program 4: Detect and Handle Outliers Using Z-Score**

Outliers can skew data. We will use the **Z-score** to identify and filter out outliers.



```python
# Python Program illustrating 
# numpy.std() method 
import numpy as np 
	
# 1D array 
arr = [18,18,19,19,20,22,55] 

print("arr : ", arr) 
print("std of arr : ", np.std(arr)) 

print ("\nMore precision with float32") 
print("std of arr : ", np.std(arr, dtype = np.float32)) 

print ("\nMore accuracy with float64") 
print("std of arr : ", np.std(arr, dtype = np.float64)) 

```

    arr :  [18, 18, 19, 19, 20, 22, 55]
    std of arr :  12.545427657200085
    
    More precision with float32
    std of arr :  12.545428
    
    More accuracy with float64
    std of arr :  12.545427657200085
    


```python
# SciPy is an open-source Python library which is used to solve scientific and mathematical problems.
from scipy import stats
import pandas as pd

url = "https://raw.githubusercontent.com/pandas-dev/pandas/master/doc/data/titanic.csv"

titanic_data = pd.read_csv(url)

# Calculate Z-scores for the 'Fare' column
# (X−mean)/std
z_scores = stats.zscore(titanic_data['Fare'].dropna())

# Filter out outliers with Z-score greater than 3 or less than -3
titanic_data = titanic_data[(z_scores < 3) & (z_scores > -3)]

# Display the first few rows of the cleaned dataset
# print(titanic_data.head())
titanic_data.head(20)

```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>PassengerId</th>
      <th>Survived</th>
      <th>Pclass</th>
      <th>Name</th>
      <th>Sex</th>
      <th>Age</th>
      <th>SibSp</th>
      <th>Parch</th>
      <th>Ticket</th>
      <th>Fare</th>
      <th>Cabin</th>
      <th>Embarked</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>1</td>
      <td>0</td>
      <td>3</td>
      <td>Braund, Mr. Owen Harris</td>
      <td>male</td>
      <td>22.0</td>
      <td>1</td>
      <td>0</td>
      <td>A/5 21171</td>
      <td>7.2500</td>
      <td>NaN</td>
      <td>S</td>
    </tr>
    <tr>
      <th>1</th>
      <td>2</td>
      <td>1</td>
      <td>1</td>
      <td>Cumings, Mrs. John Bradley (Florence Briggs Th...</td>
      <td>female</td>
      <td>38.0</td>
      <td>1</td>
      <td>0</td>
      <td>PC 17599</td>
      <td>71.2833</td>
      <td>C85</td>
      <td>C</td>
    </tr>
    <tr>
      <th>2</th>
      <td>3</td>
      <td>1</td>
      <td>3</td>
      <td>Heikkinen, Miss Laina</td>
      <td>female</td>
      <td>26.0</td>
      <td>0</td>
      <td>0</td>
      <td>STON/O2. 3101282</td>
      <td>7.9250</td>
      <td>NaN</td>
      <td>S</td>
    </tr>
    <tr>
      <th>3</th>
      <td>4</td>
      <td>1</td>
      <td>1</td>
      <td>Futrelle, Mrs. Jacques Heath (Lily May Peel)</td>
      <td>female</td>
      <td>35.0</td>
      <td>1</td>
      <td>0</td>
      <td>113803</td>
      <td>53.1000</td>
      <td>C123</td>
      <td>S</td>
    </tr>
    <tr>
      <th>4</th>
      <td>5</td>
      <td>0</td>
      <td>3</td>
      <td>Allen, Mr. William Henry</td>
      <td>male</td>
      <td>35.0</td>
      <td>0</td>
      <td>0</td>
      <td>373450</td>
      <td>8.0500</td>
      <td>NaN</td>
      <td>S</td>
    </tr>
    <tr>
      <th>5</th>
      <td>6</td>
      <td>0</td>
      <td>3</td>
      <td>Moran, Mr. James</td>
      <td>male</td>
      <td>NaN</td>
      <td>0</td>
      <td>0</td>
      <td>330877</td>
      <td>8.4583</td>
      <td>NaN</td>
      <td>Q</td>
    </tr>
    <tr>
      <th>6</th>
      <td>7</td>
      <td>0</td>
      <td>1</td>
      <td>McCarthy, Mr. Timothy J</td>
      <td>male</td>
      <td>54.0</td>
      <td>0</td>
      <td>0</td>
      <td>17463</td>
      <td>51.8625</td>
      <td>E46</td>
      <td>S</td>
    </tr>
    <tr>
      <th>7</th>
      <td>8</td>
      <td>0</td>
      <td>3</td>
      <td>Palsson, Master Gosta Leonard</td>
      <td>male</td>
      <td>2.0</td>
      <td>3</td>
      <td>1</td>
      <td>349909</td>
      <td>21.0750</td>
      <td>NaN</td>
      <td>S</td>
    </tr>
    <tr>
      <th>8</th>
      <td>9</td>
      <td>1</td>
      <td>3</td>
      <td>Johnson, Mrs. Oscar W (Elisabeth Vilhelmina Berg)</td>
      <td>female</td>
      <td>27.0</td>
      <td>0</td>
      <td>2</td>
      <td>347742</td>
      <td>11.1333</td>
      <td>NaN</td>
      <td>S</td>
    </tr>
    <tr>
      <th>9</th>
      <td>10</td>
      <td>1</td>
      <td>2</td>
      <td>Nasser, Mrs. Nicholas (Adele Achem)</td>
      <td>female</td>
      <td>14.0</td>
      <td>1</td>
      <td>0</td>
      <td>237736</td>
      <td>30.0708</td>
      <td>NaN</td>
      <td>C</td>
    </tr>
    <tr>
      <th>10</th>
      <td>11</td>
      <td>1</td>
      <td>3</td>
      <td>Sandstrom, Miss Marguerite Rut</td>
      <td>female</td>
      <td>4.0</td>
      <td>1</td>
      <td>1</td>
      <td>PP 9549</td>
      <td>16.7000</td>
      <td>G6</td>
      <td>S</td>
    </tr>
    <tr>
      <th>11</th>
      <td>12</td>
      <td>1</td>
      <td>1</td>
      <td>Bonnell, Miss Elizabeth</td>
      <td>female</td>
      <td>58.0</td>
      <td>0</td>
      <td>0</td>
      <td>113783</td>
      <td>26.5500</td>
      <td>C103</td>
      <td>S</td>
    </tr>
    <tr>
      <th>12</th>
      <td>13</td>
      <td>0</td>
      <td>3</td>
      <td>Saundercock, Mr. William Henry</td>
      <td>male</td>
      <td>20.0</td>
      <td>0</td>
      <td>0</td>
      <td>A/5. 2151</td>
      <td>8.0500</td>
      <td>NaN</td>
      <td>S</td>
    </tr>
    <tr>
      <th>13</th>
      <td>14</td>
      <td>0</td>
      <td>3</td>
      <td>Andersson, Mr. Anders Johan</td>
      <td>male</td>
      <td>39.0</td>
      <td>1</td>
      <td>5</td>
      <td>347082</td>
      <td>31.2750</td>
      <td>NaN</td>
      <td>S</td>
    </tr>
    <tr>
      <th>14</th>
      <td>15</td>
      <td>0</td>
      <td>3</td>
      <td>Vestrom, Miss Hulda Amanda Adolfina</td>
      <td>female</td>
      <td>14.0</td>
      <td>0</td>
      <td>0</td>
      <td>350406</td>
      <td>7.8542</td>
      <td>NaN</td>
      <td>S</td>
    </tr>
    <tr>
      <th>15</th>
      <td>16</td>
      <td>1</td>
      <td>2</td>
      <td>Hewlett, Mrs. (Mary D Kingcome)</td>
      <td>female</td>
      <td>55.0</td>
      <td>0</td>
      <td>0</td>
      <td>248706</td>
      <td>16.0000</td>
      <td>NaN</td>
      <td>S</td>
    </tr>
    <tr>
      <th>16</th>
      <td>17</td>
      <td>0</td>
      <td>3</td>
      <td>Rice, Master Eugene</td>
      <td>male</td>
      <td>2.0</td>
      <td>4</td>
      <td>1</td>
      <td>382652</td>
      <td>29.1250</td>
      <td>NaN</td>
      <td>Q</td>
    </tr>
    <tr>
      <th>17</th>
      <td>18</td>
      <td>1</td>
      <td>2</td>
      <td>Williams, Mr. Charles Eugene</td>
      <td>male</td>
      <td>NaN</td>
      <td>0</td>
      <td>0</td>
      <td>244373</td>
      <td>13.0000</td>
      <td>NaN</td>
      <td>S</td>
    </tr>
    <tr>
      <th>18</th>
      <td>19</td>
      <td>0</td>
      <td>3</td>
      <td>Vander Planke, Mrs. Julius (Emelia Maria Vande...</td>
      <td>female</td>
      <td>31.0</td>
      <td>1</td>
      <td>0</td>
      <td>345763</td>
      <td>18.0000</td>
      <td>NaN</td>
      <td>S</td>
    </tr>
    <tr>
      <th>19</th>
      <td>20</td>
      <td>1</td>
      <td>3</td>
      <td>Masselmani, Mrs. Fatima</td>
      <td>female</td>
      <td>NaN</td>
      <td>0</td>
      <td>0</td>
      <td>2649</td>
      <td>7.2250</td>
      <td>NaN</td>
      <td>C</td>
    </tr>
  </tbody>
</table>
</div>



**Explanation:**
- **Z-scores** measure how far a data point is from the **mean** in terms of **standard deviations**. Outliers with **Z-score > 3** or **Z-score < -3** are removed.

##### **Program 5: Detect and Handle Outliers Using IQR (Interquartile Range)**

Another method to handle outliers is the **IQR method**.




```python
import pandas as pd

url = "https://raw.githubusercontent.com/pandas-dev/pandas/master/doc/data/titanic.csv"

titanic_data = pd.read_csv(url)

# Calculate IQR for 'Fare'
Q1 = titanic_data['Fare'].quantile(0.25)
Q3 = titanic_data['Fare'].quantile(0.75)
IQR = Q3 - Q1

print(IQR)

# Filter out outliers using IQR
titanic_data = titanic_data[(titanic_data['Fare'] >= (Q1 - 1.5 * IQR)) & (titanic_data['Fare'] <= (Q3 + 1.5 * IQR))]

# # Display the first few rows of the dataset after removing outliers
# print(titanic_data.head())
titanic_data['Fare']


```

    23.0896
    




    0       7.2500
    2       7.9250
    3      53.1000
    4       8.0500
    5       8.4583
            ...   
    886    13.0000
    887    30.0000
    888    23.4500
    889    30.0000
    890     7.7500
    Name: Fare, Length: 775, dtype: float64



**Explanation:**
- **IQR** is the range between the **1st** and **3rd quartiles**. Outliers are defined as values that fall outside **1.5 times the IQR** from the **Q1** or **Q3**.


### **3. Data Transformation**

**Theory (Brief):**  

Data transformation is an essential step in preparing data for machine learning models. This process includes feature engineering, scaling/normalization, and categorical encoding. It ensures that our data is in a suitable format for algorithms to learn effectively.

---



### **1. Feature Engineering**

Feature engineering is about creating new features that are useful for model training. In this case, we're calculating `TotalRevenue` and `FamilySize`.

---

#### **Manual Calculation 1: TotalRevenue = Quantity * Price (Hypothetical Dataset)**

**Formula**:
$$
\text{TotalRevenue} = \text{Quantity} \times \text{Price}
$$

**Given**:
| Quantity | Price |  
|----------|-------|  
| 2        | 100   |  
| 5        | 60    |  
| 1        | 150   |  

**Calculations**:
- For the first row:  
$$
\text{TotalRevenue} = 2 \times 100 = 200
$$
- For the second row:  
$$
\text{TotalRevenue} = 5 \times 60 = 300
$$
- For the third row:  
$$
\text{TotalRevenue} = 1 \times 150 = 150
$$

---

#### **Manual Calculation 2: FamilySize = SibSp + Parch + 1 (Titanic Dataset)**

**Formula**:
$$
\text{FamilySize} = \text{SibSp} + \text{Parch} + 1
$$

**Given** (Titanic Dataset):
| SibSp | Parch |  
|-------|-------|  
| 1     | 0     |  
| 1     | 2     |  
| 0     | 0     |  

**Calculations**:
- For the first row:  
$$
\text{FamilySize} = 1 + 0 + 1 = 2
$$
- For the second row:  
$$
\text{FamilySize} = 1 + 2 + 1 = 4
$$
- For the third row:  
$$
\text{FamilySize} = 0 + 0 + 1 = 1
$$

---

### **2. Scaling & Normalization**

Scaling is essential for ensuring that all features have the same range, especially when working with machine learning algorithms that depend on distance or gradient descent.

---

#### **Manual Calculation 1: StandardScaler (Hypothetical Dataset)**

**Formula** for Standardization:
$$
Z = \frac{X - \mu}{\sigma}
$$
Where:
- \( X \) is the data point.
- \( \mu \) is the mean of the dataset.
- \( \sigma \) is the standard deviation of the dataset.

**Given**:
| Quantity |  
|----------|  
| 10       |  
| 20       |  
| 30       |  

**Steps**:

1. **Calculate Mean** ($ \mu $):  
$$
\mu = \frac{(10 + 20 + 30)}{3} = 20
$$

2. **Calculate Standard Deviation** ($ \sigma $):  

**Formula of Standard Deviation:**
$$
s = \sqrt{\frac{1}{n - 1} \sum_{i=1}^{n} (x_i - \bar{x})^2}
$$
$$
\sigma = \sqrt{\frac{(10-20)^2 + (20-20)^2 + (30-20)^2}{3}} = \sqrt{\frac{100 + 0 + 100}{3}} = \sqrt{\frac{200}{3}} \approx 8.16496
$$

3. **Apply Standardization Formula**:
- For \( X = 10 \):
$$
Z = \frac{10 - 20}{8.16496} \approx -1.2247
$$
- For \( X = 20 \):
$$
Z = \frac{20 - 20}{8.16496} = 0
$$
- For \( X = 30 \):
$$
Z = \frac{30 - 20}{8.16496} \approx 1.2247
$$

---

#### **Manual Calculation 2: MinMaxScaler (Hypothetical Dataset)**

**Formula**:
$$
X_{\text{scaled}} = \frac{X - X_{\text{min}}}{X_{\text{max}} - X_{\text{min}}}
$$
Where:
- \( X \) is the data point.
- \($ X_{\text{min}} $\) is the minimum value of the dataset.
- \($ X_{\text{max}} $\) is the maximum value of the dataset.

**Given**:
| Quantity |  
|----------|  
| 10       |  
| 20       |  
| 30       |  

**Steps**:

1. **Identify Min and Max Values**:
   - \($ X_{\text{min}}$ = 10 \)
   - \($ X_{\text{max}}$ = 30 \)

2. **Apply MinMax Formula**:
- For \( X = 10 \):
$$
X_{\text{scaled}} = \frac{10 - 10}{30 - 10} = 0
$$
- For \( X = 20 \):
$$
X_{\text{scaled}} = \frac{20 - 10}{30 - 10} = 0.5
$$
- For \( X = 30 \):
$$
X_{\text{scaled}} = \frac{30 - 10}{30 - 10} = 1
$$

---

### **3. Categorical Encoding**

Categorical encoding is used to convert non-numerical categories into numerical values. This is essential because machine learning algorithms can only work with numbers.

---

#### **Manual Calculation 1: Label Encoding (Hypothetical Dataset)**

**Formula**:
Assign numerical labels to each unique category in the dataset.

**Given**:
| Gender |  
|--------|  
| Male   |  
| Female |  
| Male   |  

**Steps**:
- **Male** → 1
- **Female** → 0

**Encoded Values**:
- [1, 0, 1]

---

#### **Manual Calculation 2: One-Hot Encoding (Hypothetical Dataset)**

**Formula**:
Create a binary column for each category and assign a 1 or 0 indicating the presence of that category.

**Given**:
| Gender |  
|--------|  
| Male   |  
| Female |  
| Female |  

**Steps**:
- **Male** → [1, 0]
- **Female** → [0, 1]

**One-Hot Encoded Dataset**:
| Male | Female |  
|------|--------|  
| 1    | 0      |  
| 0    | 1      |  
| 0    | 1      |

---


##### **Other Way**


#### **3.1. Feature Engineering**
Feature engineering involves creating new meaningful features from existing data to help the model understand better.


##### **Program 1: Create a New Feature (Total Fare)**

We’ll create a new feature called **TotalFare**, which is the **product of 'Fare'** and **'FamilySize'**.


```python
import pandas as pd

url = "https://raw.githubusercontent.com/pandas-dev/pandas/master/doc/data/titanic.csv"

titanic_data = pd.read_csv(url)

# Create a new feature 'TotalFare'
titanic_data['FamilySize'] = titanic_data['SibSp'] + titanic_data['Parch']
titanic_data['TotalFare'] = titanic_data['Fare'] * titanic_data['FamilySize']

# Display the first few rows of the dataset with the new feature
# print(titanic_data.head())
print(titanic_data['FamilySize'])
print(titanic_data['TotalFare'])


```

    0      1
    1      1
    2      0
    3      1
    4      0
          ..
    886    0
    887    0
    888    3
    889    0
    890    0
    Name: FamilySize, Length: 891, dtype: int64
    0       7.2500
    1      71.2833
    2       0.0000
    3      53.1000
    4       0.0000
            ...   
    886     0.0000
    887     0.0000
    888    70.3500
    889     0.0000
    890     0.0000
    Name: TotalFare, Length: 891, dtype: float64
    

**Explanation:**
- We create a **TotalFare** feature by multiplying **Fare** and **FamilySize** (calculated by adding **SibSp** and **Parch**).

##### **Program 2: Normalize 'Fare' Using Min-Max Scaling**

To normalize the **'Fare'** column, we use **Min-Max Scaling** to scale it between **0 and 1**.



```python
from sklearn.preprocessing import MinMaxScaler
import pandas as pd

url = "https://raw.githubusercontent.com/pandas-dev/pandas/master/doc/data/titanic.csv"

titanic_data = pd.read_csv(url)

# Apply Min-Max Scaling on 'Fare' column
scaler = MinMaxScaler()
titanic_data['Fare_Normalized'] = scaler.fit_transform(titanic_data[['Fare']])

# Display the first few rows with the normalized feature
print(titanic_data[['Fare', 'Fare_Normalized']].head())

```

          Fare  Fare_Normalized
    0   7.2500         0.014151
    1  71.2833         0.139136
    2   7.9250         0.015469
    3  53.1000         0.103644
    4   8.0500         0.015713
    


```python
from sklearn.preprocessing import MinMaxScaler
import pandas as pd

# Example data
df = pd.DataFrame({'Value': [10,20,30,40,50,60,70,80,90,100]})

scaler = MinMaxScaler(feature_range=(0,1))
df['Scaled'] = scaler.fit_transform(df[['Value']])

print(df)

```

       Value    Scaled
    0     10  0.000000
    1     20  0.111111
    2     30  0.222222
    3     40  0.333333
    4     50  0.444444
    5     60  0.555556
    6     70  0.666667
    7     80  0.777778
    8     90  0.888889
    9    100  1.000000
    

**Explanation:**
- **Min-Max Scaling** transforms **Fare** to a range between **0 and 1**, which helps in situations where features have different scales.

##### **Program 3: One-Hot Encoding for 'Embarked'**

We will convert the **'Embarked'** column (categorical) into numerical format using **One-Hot Encoding**.



```python
import pandas as pd

url = "https://raw.githubusercontent.com/pandas-dev/pandas/master/doc/data/titanic.csv"

titanic_data = pd.read_csv(url)

# One-Hot Encoding for 'Embarked' column
titanic_data_encoded = pd.get_dummies(titanic_data, columns=['Embarked'])

# Display the first few rows of the encoded dataset
titanic_data_encoded

```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>PassengerId</th>
      <th>Survived</th>
      <th>Pclass</th>
      <th>Name</th>
      <th>Sex</th>
      <th>Age</th>
      <th>SibSp</th>
      <th>Parch</th>
      <th>Ticket</th>
      <th>Fare</th>
      <th>Cabin</th>
      <th>Embarked_C</th>
      <th>Embarked_Q</th>
      <th>Embarked_S</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>1</td>
      <td>0</td>
      <td>3</td>
      <td>Braund, Mr. Owen Harris</td>
      <td>male</td>
      <td>22.0</td>
      <td>1</td>
      <td>0</td>
      <td>A/5 21171</td>
      <td>7.2500</td>
      <td>NaN</td>
      <td>False</td>
      <td>False</td>
      <td>True</td>
    </tr>
    <tr>
      <th>1</th>
      <td>2</td>
      <td>1</td>
      <td>1</td>
      <td>Cumings, Mrs. John Bradley (Florence Briggs Th...</td>
      <td>female</td>
      <td>38.0</td>
      <td>1</td>
      <td>0</td>
      <td>PC 17599</td>
      <td>71.2833</td>
      <td>C85</td>
      <td>True</td>
      <td>False</td>
      <td>False</td>
    </tr>
    <tr>
      <th>2</th>
      <td>3</td>
      <td>1</td>
      <td>3</td>
      <td>Heikkinen, Miss Laina</td>
      <td>female</td>
      <td>26.0</td>
      <td>0</td>
      <td>0</td>
      <td>STON/O2. 3101282</td>
      <td>7.9250</td>
      <td>NaN</td>
      <td>False</td>
      <td>False</td>
      <td>True</td>
    </tr>
    <tr>
      <th>3</th>
      <td>4</td>
      <td>1</td>
      <td>1</td>
      <td>Futrelle, Mrs. Jacques Heath (Lily May Peel)</td>
      <td>female</td>
      <td>35.0</td>
      <td>1</td>
      <td>0</td>
      <td>113803</td>
      <td>53.1000</td>
      <td>C123</td>
      <td>False</td>
      <td>False</td>
      <td>True</td>
    </tr>
    <tr>
      <th>4</th>
      <td>5</td>
      <td>0</td>
      <td>3</td>
      <td>Allen, Mr. William Henry</td>
      <td>male</td>
      <td>35.0</td>
      <td>0</td>
      <td>0</td>
      <td>373450</td>
      <td>8.0500</td>
      <td>NaN</td>
      <td>False</td>
      <td>False</td>
      <td>True</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>886</th>
      <td>887</td>
      <td>0</td>
      <td>2</td>
      <td>Montvila, Rev. Juozas</td>
      <td>male</td>
      <td>27.0</td>
      <td>0</td>
      <td>0</td>
      <td>211536</td>
      <td>13.0000</td>
      <td>NaN</td>
      <td>False</td>
      <td>False</td>
      <td>True</td>
    </tr>
    <tr>
      <th>887</th>
      <td>888</td>
      <td>1</td>
      <td>1</td>
      <td>Graham, Miss Margaret Edith</td>
      <td>female</td>
      <td>19.0</td>
      <td>0</td>
      <td>0</td>
      <td>112053</td>
      <td>30.0000</td>
      <td>B42</td>
      <td>False</td>
      <td>False</td>
      <td>True</td>
    </tr>
    <tr>
      <th>888</th>
      <td>889</td>
      <td>0</td>
      <td>3</td>
      <td>Johnston, Miss Catherine Helen "Carrie"</td>
      <td>female</td>
      <td>NaN</td>
      <td>1</td>
      <td>2</td>
      <td>W./C. 6607</td>
      <td>23.4500</td>
      <td>NaN</td>
      <td>False</td>
      <td>False</td>
      <td>True</td>
    </tr>
    <tr>
      <th>889</th>
      <td>890</td>
      <td>1</td>
      <td>1</td>
      <td>Behr, Mr. Karl Howell</td>
      <td>male</td>
      <td>26.0</td>
      <td>0</td>
      <td>0</td>
      <td>111369</td>
      <td>30.0000</td>
      <td>C148</td>
      <td>True</td>
      <td>False</td>
      <td>False</td>
    </tr>
    <tr>
      <th>890</th>
      <td>891</td>
      <td>0</td>
      <td>3</td>
      <td>Dooley, Mr. Patrick</td>
      <td>male</td>
      <td>32.0</td>
      <td>0</td>
      <td>0</td>
      <td>370376</td>
      <td>7.7500</td>
      <td>NaN</td>
      <td>False</td>
      <td>True</td>
      <td>False</td>
    </tr>
  </tbody>
</table>
<p>891 rows × 14 columns</p>
</div>




```python
# import pandas as pd
# from sklearn.preprocessing import OneHotEncoder

# sm = OneHotEncoder()

# # Sample data
# data = {
#     'Color': ['Red', 'Blue', 'Green', 'Blue', 'Red','Gold']
# }
# df = pd.DataFrame(data)

# sm.fit(df['Color'])
# ohe = sm.transform(sparse_output=False)
# ohe.toarray()
# # print(ohe)

import pandas as pd
from sklearn.preprocessing import OneHotEncoder

# Sample data
data = {
    'Color': ['Red', 'Blue', 'Green', 'Blue', 'Red', 'Gold']
}

# Convert the data into a DataFrame
df = pd.DataFrame(data)

# Initialize the OneHotEncoder
sm = OneHotEncoder(sparse_output=False)  # Use sparse=False to get a dense array

# Fit the encoder on the 'Color' column (reshaping to 2D)
sm.fit(df[['Color']])  # Use double brackets to keep it as a DataFrame

# Transform the data
ohe = sm.transform(df[['Color']])

# Convert the result to an array and print it
print(ohe)
```

    [[0. 0. 0. 1.]
     [1. 0. 0. 0.]
     [0. 0. 1. 0.]
     [1. 0. 0. 0.]
     [0. 0. 0. 1.]
     [0. 1. 0. 0.]]
    


```python
import pandas as pd
from sklearn.preprocessing import OneHotEncoder

# Sample data
data = {
    'Color': ['Red', 'Blue', 'Green', 'Blue', 'Red','Gold'],
    'Size': ['S', 'M', 'L', 'M', 'S','M']
}

# Create a DataFrame
df = pd.DataFrame(data)

# Display the original DataFrame
# print("Original DataFrame:")
# print(df)

# # Method 1: Using pandas get_dummies
# df_onehot_pandas = pd.get_dummies(df, columns=['Color', 'Size'], drop_first=True)

# # Display the one-hot encoded DataFrame using pandas
# print("\nOne-Hot Encoded DataFrame using pandas:")
# print(df_onehot_pandas)

# Method 2: Using sklearn OneHotEncoder
encoder = OneHotEncoder(sparse_output=False, drop=None)
encoded_array = encoder.fit_transform(df[['Color', 'Size']])

print(encoded_array)

# Create a DataFrame with the encoded features
encoded_df = pd.DataFrame(encoded_array, columns=encoder.get_feature_names_out(['Color', 'Size']))

# Display the one-hot encoded DataFrame using sklearn
print("\nOne-Hot Encoded DataFrame using sklearn:")
print(encoded_df)

# data = {
#     'Color': ['Red', 'Blue', 'Green', 'Blue', 'Red'],
#     'Size': ['S', 'M', 'L', 'M', 'S']
# }
```

    [[0. 0. 0. 1. 0. 0. 1.]
     [1. 0. 0. 0. 0. 1. 0.]
     [0. 0. 1. 0. 1. 0. 0.]
     [1. 0. 0. 0. 0. 1. 0.]
     [0. 0. 0. 1. 0. 0. 1.]
     [0. 1. 0. 0. 0. 1. 0.]]
    
    One-Hot Encoded DataFrame using sklearn:
       Color_Blue  Color_Gold  Color_Green  Color_Red  Size_L  Size_M  Size_S
    0         0.0         0.0          0.0        1.0     0.0     0.0     1.0
    1         1.0         0.0          0.0        0.0     0.0     1.0     0.0
    2         0.0         0.0          1.0        0.0     1.0     0.0     0.0
    3         1.0         0.0          0.0        0.0     0.0     1.0     0.0
    4         0.0         0.0          0.0        1.0     0.0     0.0     1.0
    5         0.0         1.0          0.0        0.0     0.0     1.0     0.0
    


```python
import pandas as pd

df = pd.DataFrame({'Color': ['Red','Green','Blue','Red']})
# df_ohe = pd.get_dummies(df, columns=['Color'], prefix='Color', drop_first=True)
df_ohe = pd.get_dummies(df, columns=['Color'], prefix='Color', drop_first=False)
print(df_ohe)

```

       Color_Blue  Color_Green  Color_Red
    0       False        False       True
    1       False         True      False
    2        True        False      False
    3       False        False       True
    

**Explanation:**
- **One-Hot Encoding** creates separate binary columns for each unique value in **'Embarked'** (e.g., C, Q, S).

##### **Program 4: Standardize 'Age' Using Z-Score**

Standardize the **'Age'** column so it has **mean = 0** and **std = 1**.



```python
from sklearn.preprocessing import StandardScaler
import pandas as pd

url = "https://raw.githubusercontent.com/pandas-dev/pandas/master/doc/data/titanic.csv"

titanic_data = pd.read_csv(url)

# Standardize 'Age' column
scaler = StandardScaler()
titanic_data['Age_Standardized'] = scaler.fit_transform(titanic_data[['Age']])

# Display the first few rows with the standardized 'Age'
print(titanic_data[['Age', 'Age_Standardized']].head())
```

        Age  Age_Standardized
    0  22.0         -0.530377
    1  38.0          0.571831
    2  26.0         -0.254825
    3  35.0          0.365167
    4  35.0          0.365167
    

**Explanation:**
- **Standardization** centers the data around **0** and scales it to a **standard deviation of 1**.

##### **Program 5: Label Encoding for 'Sex'**

Convert the **'Sex'** column to numerical values using **Label Encoding**.



```python
from sklearn.preprocessing import LabelEncoder
import pandas as pd

url = "https://raw.githubusercontent.com/pandas-dev/pandas/master/doc/data/titanic.csv"

titanic_data = pd.read_csv(url)
# Label Encoding for 'Sex' column
label_encoder = LabelEncoder()
titanic_data['Sex_Encoded'] = label_encoder.fit_transform(titanic_data['Sex'])

# Display the first few rows with the encoded 'Sex'
print(titanic_data[['Sex', 'Sex_Encoded']].head())

```

          Sex  Sex_Encoded
    0    male            1
    1  female            0
    2  female            0
    3  female            0
    4    male            1
    


```python
# import pandas as pd

# df = pd.DataFrame({'Color': ['Red','Green','Blue','Red']})
# df['Color_Label'], uniques = pd.factorize(df['Color'])
# print(df)
# # uniques array shown as 0→'Red', 1→'Green', 2→'Blue'

from sklearn.preprocessing import LabelEncoder
import pandas as pd

df = pd.DataFrame({'Color': ['Red','Green','Blue','Red']})
le = LabelEncoder()
df['Color_Label'] = le.fit_transform(df['Color'])
print(df)
# le.classes_ will be shown ['Blue','Green','Red']

```

       Color  Color_Label
    0    Red            2
    1  Green            1
    2   Blue            0
    3    Red            2
    


**Explanation:**
- **Label Encoding** assigns each unique category (Male = 0, Female = 1) in **'Sex'** to a **numerical value**.


## **Exploratory Data Analysis (EDA)**

### **Introduction to EDA**
Exploratory Data Analysis (EDA) is an essential step in the data science pipeline, helping analysts and data scientists to understand the dataset before applying any machine learning algorithms or statistical models. The goal of EDA is to:
- Summarize the key characteristics of the data.
- Visualize data distributions and relationships between features.
- Detect outliers or anomalies.
- Identify trends or patterns that can influence model building.

we will explore the following tasks in detail:
1. **Descriptive Statistics**
2. **Data Visualization**

We will work with two types of datasets:
- **Hypothetical Datasets**: Simulated data to demonstrate calculations and analysis.
- **Real Datasets**: A dataset like **Titanic** to show how to perform the analysis on actual data.

---

### **1. Descriptive Statistics**

Descriptive statistics involve calculating key metrics that summarize the central tendency, spread, and shape of the data. The main methods used are:
- **Mean, Median, and Mode**: Measures of central tendency.
- **Variance and Standard Deviation**: Measures of spread or variability.
- **Skewness and Kurtosis**: Measures of the shape of the distribution.

---

#### **1.1 Hypothetical Dataset**: Sales Data
We will work with a small dataset representing **Customer Purchase Prices**.

| Customer ID | Purchase Price |  
|-------------|----------------|  
| 1           | 100            |  
| 2           | 200            |  
| 3           | 150            |  
| 4           | 300            |  
| 5           | 250            |  

**Manual Calculation**:

1. **Mean**:
$$
\text{Mean} = \frac{100 + 200 + 150 + 300 + 250}{5} = \frac{1000}{5} = 200
$$

2. **Median**:
Since there are 5 data points, the median is the middle value:
$$
\text{Median} = 200 \, (\text{3rd value})
$$

3. **Mode**:
Since there are no repeating values, there is no mode.

4. **Variance**:
$$
\text{Variance} = \frac{(100 - 200)^2 + (200 - 200)^2 + (150 - 200)^2 + (300 - 200)^2 + (250 - 200)^2}{5}
$$
$$
\text{Variance} = \frac{10000 + 0 + 2500 + 10000 + 2500}{5} = \frac{25000}{5} = 5000
$$

5. **Standard Deviation**:
$$
\text{Standard Deviation} = \sqrt{5000} \approx 70.71
$$

---
#### **1.2 Program for Hypothetical Dataset**:


```python
import pandas as pd

# Hypothetical Dataset
data = {'Customer ID': [1, 2, 3, 4, 5], 'Purchase Price': [100, 200, 150, 300, 250]}
df = pd.DataFrame(data)
# print(df)

# Descriptive Statistics
mean = df['Purchase Price'].mean()
median = df['Purchase Price'].median()
mode = df['Purchase Price'].mode()[0]  # Using mode()[0] to get the first mode
# if we calculatiing large dataset full of papulation values so we use ddof=0 (degree of freedom)
variance = df['Purchase Price'].var(ddof=0)
std_dev = df['Purchase Price'].std(ddof=0)
# Otherwise, default ddof=1 is correct when estimating for a larger unknown population for sample estimating dataset
# variance = df['Purchase Price'].var()
# std_dev = df['Purchase Price'].std()
print(f"Mean: {mean}, Median: {median}, Mode: {mode}, Variance: {variance}, Standard Deviation: {std_dev}")
# print(df['Purchase Price'].mode())

```

    Mean: 200.0, Median: 200.0, Mode: 100, Variance: 5000.0, Standard Deviation: 70.71067811865476
    


#### **1.3 Real Dataset (Titanic)**:  
Now, let's analyze the **Titanic dataset**. We'll calculate the **mean** age and **standard deviation** of the ages of passengers.

**Manual Calculation**:
For simplicity, let's say we have the following `Age` values from the Titanic dataset:

| Age |  
|-----|  
| 22  |  
| 38  |  
| 26  |  
| 35  |  
| 54  |  

1. **Mean**:
$$
\text{Mean} = \frac{22 + 38 + 26 + 35 + 54}{5} = \frac{175}{5} = 35
$$

2. **Standard Deviation**:
First, calculate the variance:
$$
\text{Variance} = \frac{(22 - 35)^2 + (38 - 35)^2 + (26 - 35)^2 + (35 - 35)^2 + (54 - 35)^2}{5}
$$
$$
\text{Variance} = \frac{169 + 9 + 81 + 0 + 361}{5} = \frac{620}{5} = 124
$$
Now, calculate the standard deviation:
$$
\text{Standard Deviation} = \sqrt{124} \approx 11.14
$$

---

#### **1.4 Program for Titanic Dataset**:


```python
import pandas as pd

# Load Titanic Dataset
df_titanic = pd.read_csv("https://raw.githubusercontent.com/pandas-dev/pandas/master/doc/data/titanic.csv")

# Descriptive Statistics for Age
mean_age = df_titanic['Age'].mean()
variance = df_titanic['Age'].var()
std_dev_age = df_titanic['Age'].std()

variance_df = df_titanic['Age'].var(ddof=0)
std_dev_age_df = df_titanic['Age'].std(ddof=0)

print(f"Mean Age: {mean_age}, Variance for Age: {variance}, Standard Deviation of Age: {std_dev_age}")
print(f"Variance with ddof {variance_df}, Std with ddof: {std_dev_age_df}")
# print(list(df_titanic['Age']))
```

    Mean Age: 29.69911764705882, Variance for Age: 211.0191247463081, Standard Deviation of Age: 14.526497332334044
    Variance with ddof 210.7235797536662, Std with ddof: 14.516321150817317
    

### **1.6. Skewness and Kurtosis**

#### **Theory (Brief)**:
- **Skewness**: It measures the asymmetry of the data distribution. A positive skew indicates the data is skewed to the right, while a negative skew indicates the data is skewed to the left.
- **Kurtosis**: It measures the "tailedness" or sharpness of the peak of the distribution. High kurtosis indicates more extreme outliers, while low kurtosis indicates fewer extreme outliers.

Both **Skewness** and **Kurtosis** help us understand the shape of the data and are essential for detecting abnormal distributions that may require transformations.

---

### **1.1 Hypothetical Dataset**: Customer Spending

We will calculate **skewness** for the following set of **customer spending values**.

| Customer ID | Spending Amount |  
|-------------|-----------------|  
| 1001        | 50              |  
| 1002        | 200             |  
| 1003        | 150             |  
| 1004        | 300             |  
| 1005        | 250             |  

---

### **Manual Calculation of Skewness**

---

### 🔹 **Step 1: Calculate the Mean** \( $ \bar{X} $\)

$$
\bar{X} = \frac{50 + 200 + 150 + 300 + 250}{5} = \frac{950}{5} = 190
$$

**Mean (𝑋̄) = 190**

---

### 🔹 **Step 2: Calculate the Sample Standard Deviation** \( s \)

Use sample standard deviation formula (ddof = 1):

$$
s = \sqrt{\frac{\sum (X_i - \bar{X})^2}{n - 1}}
$$

Let’s compute squared differences:

| $ ( X_i $\) | $  ( X_i - \bar{X} $\) | $  (X_i - \bar{X})^2 $ \) |
|----------|---------------------|--------------------------|
| 50       | 50 - 190 = -140                | 19600                    |
| 200      | 200 - 190 = 10                  | 100                      |
| 150      | 150 - 190 = -40                 | 1600                     |
| 300      | 300 - 190 = 110                 | 12100                    |
| 250      | 250 - 190 = 60                  | 3600                     |

Total sum of squares:

$$
\sum (X_i - \bar{X})^2 = 19600 + 100 + 1600 + 12100 + 3600 = 37000
$$

$$
s = \sqrt{\frac{37000}{5 - 1}} = \sqrt{9250} \approx 96.18
$$

**Sample Standard Deviation (s) ≈ 96.18**

---

### 🔹 **Step 3: Calculate the Skewness**

Use **sample skewness** formula:

$$
\text{Skewness} = \frac{n}{(n - 1)(n - 2)} \sum \frac{(X_i - \bar{X})^3}{s^3}
$$

Let’s compute cubed differences:

| \($ X_i $\) | \($ X_i - \bar{X} $\) | \($ (X_i - \bar{X})^3 $\)     |
|----------|---------------------|-----------------------------|
| 50       | 50 - 190 = -140                | -2,744,000                  |
| 200      | 200 - 190 = 10                  | 1,000                       |
| 150      | 150 - 190 = -40                 | -64,000                     |
| 300      | 300 - 190 = 110                 | 1,331,000                   |
| 250      | 250 - 190 = 60                  | 216,000                     |

Total sum of cubes:

$$
\sum (X_i - \bar{X})^3 = -2744000 + 1000 - 64000 + 1331000 + 216000 = -1,260,000
$$

Now plug into skewness formula:

- \( n = 5 \)
- \( s^3 = 96.18^3 ≈ 889700 \)

$$
\text{Skewness} = \frac{5}{(5-1)(5-2)} \cdot \frac{-1260000}{889700}
= \frac{5}{12} \cdot (-1.416) ≈ -0.5901
$$

**Final Skewness ≈ −0.5901**

---

### **Interpretation**:
Since **skewness < 0**, the distribution is **left-skewed (negatively skewed)**. This means more data is concentrated on the higher end (right side), with a longer tail on the left side.


#### **1.4 Program for Skewness Calculation**:



```python
import pandas as pd

data = {
    'Customer ID': [1001, 1002, 1003, 1004, 1005],
    'Spending Amount': [50, 200, 150, 300, 250]
}
df = pd.DataFrame(data)

# Calculate Skewness
skewness = df['Spending Amount'].skew()

print("Skewness:", skewness)

```

    Skewness: -0.5901286563843656
    


```python
import numpy as np

data = [50, 200, 150, 300, 250]
mean = np.mean(data)
std = np.std(data)  # default ddof=0

manual_skew = (1/len(data)) * sum(((x - mean)/std)**3 for x in data)
print("Manual (population) skew:", manual_skew)

```

    Manual (population) skew: -0.39587033734381666
    


```python
from scipy.stats import skew

data = [50, 200, 150, 300, 250]
print("Scipy skew (bias-corrected):", skew(data, bias=False))

```

    Scipy skew (bias-corrected): -0.5901286563843656
    


##  **1.7 Kurtosis**
Kurtosis measures the **tailedness** of a data distribution. High kurtosis = heavy tails; low kurtosis = light tails.

We will use **sample excess kurtosis** formula (without bias), which compares to normal distribution (kurtosis of 3):

---

### **Hypothetical Dataset**: Customer Spending

| Customer ID | Spending Amount |  
|-------------|-----------------|  
| 1001        | 50              |  
| 1002        | 200             |  
| 1003        | 150             |  
| 1004        | 300             |  
| 1005        | 250             |  

---



### **Step 1: Mean ($ \bar{X} $)**

Already calculated earlier:

$
\bar{X} = 190
$

---

### **Step 2: Sample Standard Deviation (s)**

Already calculated:

$
s = 96.18
$

---

### **Step 3: Kurtosis Formula**

Sample **excess kurtosis** (Fisher’s definition):

$
\text{Kurtosis} = \frac{n(n+1)}{(n-1)(n-2)(n-3)} \sum \left( \frac{(X_i - \bar{X})^4}{s^4} \right) - \frac{3(n-1)^2}{(n-2)(n-3)}
$

---

###  Step-by-step Calculation:

| \($ X_i $ \) | \($ X_i $ - $ \bar{X} $\) | \( ($ X_i $ - $ \bar{X})^4$ \) |
|----------|----------------------|--------------------------|
| 50       | -140                 | 384160000                |
| 200      | 10                   | 10000                    |
| 150      | -40                  | 2560000                  |
| 300      | 110                  | 146410000                |
| 250      | 60                   | 12960000                 |

Total: <br>
$
\sum (X_i - \bar{X})^4 = 384160000 + 10000 + 2560000 + 146410000 + 12960000 = 545790000
$

---

###  Step 4: Plug into Kurtosis Formula

- \( n = 5 \)
- \($ s^4 $ = $ (96.18)^4 $ ≈ 85548609 \)

$
\text{Term1} = \frac{5(5+1)}{(5-1)(5-2)(5-3)} \cdot \frac{545790000}{85548609}
= \frac{30}{24} \cdot 6.382 ≈ 1.25 \cdot 6.382 ≈ 7.977
$

$
\text{Term2} = \frac{3(5 - 1)^2}{(5 - 2)(5 - 3)} = \frac{3(16)}{3 \cdot 2} = \frac{48}{6} = 8
$

---

###  Final Excess Kurtosis:

$
\text{Kurtosis} = 7.977 - 8 ≈ -0.023
$

---

### **Interpretation**:

- **Kurtosis ≈ -0.023** → Very close to 0 ⇒  
  → The distribution is **approximately mesokurtic**  
  → Tails are almost normal, no extreme peaks or outliers.

---


### 🤝 Summary:

| Metric     | Value    | Interpretation                     |
|------------|----------|-------------------------------------|
| Mean       | 190      | Central value                      |
| Std Dev    | 96.18    | Spread of values                   |
| Skewness   | -0.5901  | Left-skewed                        |
| Kurtosis   | -0.023   | Normal-like tails (mesokurtic)     |



```python
import numpy as np
from scipy.stats import kurtosis

spending = np.array([50, 200, 150, 300, 250])

# Excess kurtosis using Fisher's definition
kurt = kurtosis(spending, fisher=True, bias=False)

print(f"Kurtosis (Excess): {kurt:.4f}")
```

    Kurtosis (Excess): -0.0219
    


```python
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
from scipy.stats import skew, kurtosis

# Create 3 types of distributions
np.random.seed(42)

# Positively skewed data (right skewed)
positive_skew = np.random.exponential(scale=2, size=1000)

# Negatively skewed data (left skewed)
negative_skew = -1 * np.random.exponential(scale=2, size=1000)

# Moderately normal data
moderate = np.random.normal(loc=0, scale=1, size=1000)

# Prepare data dictionary
data_sets = {
    "Positive Skew": positive_skew,
    "Negative Skew": negative_skew,
    "Moderate / Normal": moderate
}

# Plotting
plt.figure(figsize=(18, 5))

for i, (title, data) in enumerate(data_sets.items(), 1):
    plt.subplot(1, 3, i)
    sns.histplot(data, bins=30, kde=True, color='skyblue', edgecolor='black')
    
    skew_val = skew(data, bias=False)
    kurt_val = kurtosis(data, fisher=True, bias=False)
    
    plt.title(f"{title}\nSkewness: {skew_val:.2f} | Kurtosis: {kurt_val:.2f}", fontsize=12)
    plt.axvline(np.mean(data), color='red', linestyle='dashed', linewidth=1.5, label='Mean')
    plt.legend()
    plt.xlabel('Value')
    plt.ylabel('Frequency')

plt.suptitle("Skewness and Kurtosis Visualization", fontsize=16)
plt.tight_layout(rect=[0, 0, 1, 0.95])
plt.show()

```


    
![png](output_54_0.png)
    



```python
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns
from scipy.stats import skew

# Your dataset
spending = np.array([50, 200, 150, 300, 250])

# Skewness value
skew_value = skew(spending)

# Plotting
plt.figure(figsize=(6, 4))
sns.histplot(spending, bins=10, kde=True, color='skyblue', edgecolor='black')
plt.axvline(np.mean(spending), color='red', linestyle='dashed', label='Mean')

# Annotate skewness
plt.title(f"Skewness Visualization\nSkewness = {skew_value:.3f}", fontsize=14)
plt.xlabel("Spending Amount")
plt.ylabel("Frequency")
plt.legend()
plt.tight_layout()
plt.show()

```


    
![png](output_55_0.png)
    



```python
from scipy.stats import kurtosis

# Kurtosis value (Fisher=True gives excess kurtosis: Normal distribution = 0)
kurt_value = kurtosis(spending, fisher=True, bias=False)

# Plotting
plt.figure(figsize=(6, 4))
sns.histplot(spending, bins=10, kde=True, color='lightgreen', edgecolor='black')
plt.axvline(np.mean(spending), color='purple', linestyle='dashed', label='Mean')

# Annotate kurtosis
plt.title(f"Kurtosis Visualization\nKurtosis = {kurt_value:.3f}", fontsize=14)
plt.xlabel("Spending Amount")
plt.ylabel("Frequency")
plt.legend()
plt.tight_layout()
plt.show()

```


    
![png](output_56_0.png)
    



```python
# Combined plot
plt.figure(figsize=(6, 4))
sns.histplot(spending, bins=10, kde=True, color='orange', edgecolor='black')
plt.axvline(np.mean(spending), color='blue', linestyle='dashed', label='Mean')

# Annotate both skewness and kurtosis
plt.title(f"Spending Distribution\nSkewness = {skew_value:.3f}, Kurtosis = {kurt:.3f}", fontsize=14)
plt.xlabel("Spending Amount")
plt.ylabel("Frequency")
plt.legend()
plt.tight_layout()
plt.show()

```


    
![png](output_57_0.png)
    



```python
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns
from scipy.stats import skew, kurtosis

# Load Titanic Dataset
url = "https://raw.githubusercontent.com/pandas-dev/pandas/master/doc/data/titanic.csv"
df = pd.read_csv(url)

# Filter numeric columns only
numeric_cols = df.select_dtypes(include='number').columns.tolist()
print(numeric_cols)

# Plotting Skewness
plt.figure(figsize=(15, 5))
for i, col in enumerate(numeric_cols, 1):
    plt.subplot(1, len(numeric_cols), i)
    sns.histplot(df[col].dropna(), kde=True, color='blue', edgecolor='black')
    skew_val = skew(df[col].dropna(), bias=False)
    plt.title(f'{col}\nSkewness: {skew_val:.2f}', fontsize=10)
    plt.xlabel(col)
    plt.ylabel("Frequency")
    plt.xticks(rotation=45)
plt.suptitle("Skewness of Titanic Dataset (Numeric Columns)", fontsize=14)
plt.tight_layout(rect=[0, 0, 1, 0.92])
plt.show()

# Plotting Kurtosis
plt.figure(figsize=(15, 5))
for i, col in enumerate(numeric_cols, 1):
    plt.subplot(1, len(numeric_cols), i)
    sns.histplot(df[col].dropna(), kde=True, color='green', edgecolor='black')
    kurt_val = kurtosis(df[col].dropna(), fisher=True, bias=False)
    plt.title(f'{col}\nKurtosis: {kurt_val:.2f}', fontsize=10)
    plt.xlabel(col)
    plt.ylabel("Frequency")
    plt.xticks(rotation=45)
plt.suptitle("Kurtosis of Titanic Dataset (Numeric Columns)", fontsize=14)
plt.tight_layout(rect=[0, 0, 1, 0.92])
plt.show()

```

    ['PassengerId', 'Survived', 'Pclass', 'Age', 'SibSp', 'Parch', 'Fare']
    


    
![png](output_58_1.png)
    



    
![png](output_58_2.png)
    


### **Pair Plots**
- **Pair Plots**: A pair plot is a matrix of scatterplots that shows the relationships between multiple continuous variables. It helps identify correlations between pairs of features and visualize trends or clusters in the data.

For example, in customer data, a pair plot can show how features like **Age**, **Income**, and **Spending** are related to one another.

---

#### **2.1 Hypothetical Dataset**: Customer Demographics

Let's create a **hypothetical dataset** for **Age**, **Income**, and **Spending**.

| Customer ID | Age | Income | Spending |  
|-------------|-----|--------|----------|  
| 1           | 22  | 35000  | 500      |  
| 2           | 30  | 45000  | 700      |  
| 3           | 25  | 38000  | 600      |  
| 4           | 35  | 55000  | 1000     |  
| 5           | 40  | 60000  | 1500     |

We will visualize the relationships between **Age**, **Income**, and **Spending** using a **pair plot**.

#### **Program for Hypothetical Dataset**:


```python
import seaborn as sns
import matplotlib.pyplot as plt

# Hypothetical Dataset
data = {
    'Age': [22, 30, 25, 35, 40],
    'Income': [35000, 45000, 38000, 55000, 60000],
    'Spending': [500, 700, 600, 1000, 1500]
}
df_customer = pd.DataFrame(data)

# Pair Plot
sns.pairplot(df_customer)
plt.suptitle("Pair Plot of Age, Income, and Spending", y=1.02)
plt.show()
```


    
![png](output_60_0.png)
    



```python
import matplotlib.pyplot as plt
import pandas as pd

# Dataset
data = {
    'Age': [22, 30, 25, 35, 40],
    'Income': [35000, 45000, 38000, 55000, 60000],
    'Spending': [500, 700, 600, 1000, 1500]
}
df = pd.DataFrame(data)

# Plotting
plt.figure(figsize=(15, 5))

# 1. Age vs Income
plt.subplot(1, 3, 1)
plt.scatter(df['Age'], df['Income'], color='blue', label='Age vs Income')
plt.xlabel('Age')
plt.ylabel('Income')
plt.title('Age vs Income')
plt.legend()

# 2. Age vs Spending
plt.subplot(1, 3, 2)
plt.scatter(df['Age'], df['Spending'], color='green', label='Age vs Spending')
plt.xlabel('Age')
plt.ylabel('Spending')
plt.title('Age vs Spending')
plt.legend()

# 3. Income vs Spending
plt.subplot(1, 3, 3)
plt.scatter(df['Income'], df['Spending'], color='red', label='Income vs Spending')
plt.xlabel('Income')
plt.ylabel('Spending')
plt.title('Income vs Spending')
plt.legend()

plt.suptitle('Custom Scatter Plots with Labels and Legends', fontsize=16)
plt.tight_layout()
plt.subplots_adjust(top=0.85)
plt.show()

```


    
![png](output_61_0.png)
    



#### **2.2 Real Dataset (Titanic)**:  
Now, let's create a **pair plot** for the **Age**, **Fare**, and **FamilySize** columns in the **Titanic dataset**.

**Steps**:
1. **Load the Titanic dataset**.
2. **Create a pair plot for Age, Fare, and FamilySize**.

#### **Program for Titanic Dataset**:


```python
import pandas as pd

# Load Titanic Dataset
df_titanic = pd.read_csv("https://raw.githubusercontent.com/pandas-dev/pandas/master/doc/data/titanic.csv")

# Add FamilySize feature
df_titanic['FamilySize'] = df_titanic['SibSp'] + df_titanic['Parch'] + 1

# Pair Plot for Age, Fare, and FamilySize
sns.pairplot(df_titanic[['Age', 'Fare', 'FamilySize']].dropna())
plt.suptitle("Pair Plot of Age, Fare, and FamilySize", y=1.02)
plt.show()
```


    
![png](output_63_0.png)
    



```python
import pandas as pd
import seaborn as sns
import matplotlib.pyplot as plt

# Load Titanic Dataset
df_titanic = pd.read_csv("https://raw.githubusercontent.com/pandas-dev/pandas/master/doc/data/titanic.csv")

# Create FamilySize feature
df_titanic['FamilySize'] = df_titanic['SibSp'] + df_titanic['Parch'] + 1

# Select features to visualize
features = ['Age', 'Fare', 'FamilySize', 'Survived']
df_clean = df_titanic[features].dropna()

# Use modern seaborn theme
sns.set(style='whitegrid', context='notebook', palette='Set2')

# Create Pair Plot (with hue='Survived' to show survival in color)
pair = sns.pairplot(
    df_clean,
    hue='Survived',
    palette={0: '#E74C3C', 1: '#2ECC71'}, # color 
    diag_kind='kde',
    corner=True,
    plot_kws={'alpha': 0.6, 's': 60, 'edgecolor': 'k'},
    diag_kws={'shade': True}
)

# Title and layout
pair.fig.suptitle('Titanic Data: Pair Plot of Age, Fare & FamilySize by Survival', fontsize=16, y=1.02)
pair.fig.subplots_adjust(top=0.92)

# Add custom legend title
new_labels = ['Did Not Survive', 'Survived']
for t, l in zip(pair._legend.texts, new_labels): 
    t.set_text(l)
pair._legend.set_title('Survival Status')

# Show Plot
plt.show()

```

    C:\Users\mrahe\anaconda3\Lib\site-packages\seaborn\axisgrid.py:1513: FutureWarning: 
    
    `shade` is now deprecated in favor of `fill`; setting `fill=True`.
    This will become an error in seaborn v0.14.0; please update your code.
    
      func(x=vector, **plot_kwargs)
    C:\Users\mrahe\anaconda3\Lib\site-packages\seaborn\axisgrid.py:1513: FutureWarning: 
    
    `shade` is now deprecated in favor of `fill`; setting `fill=True`.
    This will become an error in seaborn v0.14.0; please update your code.
    
      func(x=vector, **plot_kwargs)
    C:\Users\mrahe\anaconda3\Lib\site-packages\seaborn\axisgrid.py:1513: FutureWarning: 
    
    `shade` is now deprecated in favor of `fill`; setting `fill=True`.
    This will become an error in seaborn v0.14.0; please update your code.
    
      func(x=vector, **plot_kwargs)
    


    
![png](output_64_1.png)
    



### **Correlation**

### **What is Correlation?**
**Correlation** refers to the statistical relationship between two variables. It helps us understand the extent to which two variables change together. The **correlation coefficient (r)** can range from -1 to 1:
- **+1**: Perfect positive correlation
- **0**: No correlation (Null Correlation)
- **-1**: Perfect negative correlation

---

### **1. High Positive Correlation**

#### **Theory**:
- **High Positive Correlation** means that as one variable increases, the other variable increases at a similar rate, and the correlation coefficient is close to 1 (but not exactly 1).

#### **Hypothetical Situation**:
- **Example**: The relationship between **study hours** and **exam scores**.
  - As students study more, their scores tend to increase.

#### **Plot and Program**:



```python
import numpy as np
import matplotlib.pyplot as plt

# Hypothetical Data: Study hours vs Exam scores
study_hours = np.array([1, 2, 3, 4, 5, 6, 7, 8, 9, 10])
exam_scores = study_hours * 10 + 30  # High positive correlation

# Scatter plot
plt.figure(figsize=(6, 4))
plt.scatter(study_hours, exam_scores, color='blue')
plt.title("High Positive Correlation: Study Hours vs Exam Scores")
plt.xlabel("Study Hours")
plt.ylabel("Exam Scores")
plt.grid(True)
plt.show()
```


    
![png](output_66_0.png)
    


**Explanation**:
- As the **study hours** increase, the **exam scores** increase, showing a **strong positive relationship**.


---

### **2. Perfect Positive Correlation**

#### **Theory**:
- **Perfect Positive Correlation** means that as one variable increases, the other increases in a perfectly linear fashion with a correlation coefficient of **1**.

#### **Hypothetical Situation**:
- **Example**: The relationship between **height (in cm)** and **height (in meters)**.
  - If one value is always exactly a factor of the other (e.g., 1 meter = 100 cm), it will have a **perfect positive correlation**.

#### **Plot and Program**:



```python
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt
# Hypothetical Data: Height in cm vs Height in meters
height_cm = np.array([100, 150, 200, 250, 300])
height_m = height_cm / 100  # Perfect positive correlation

# Scatter plot
plt.figure(figsize=(6, 4))
plt.scatter(height_cm, height_m, color='green')
plt.title("Perfect Positive Correlation: Height in cm vs Height in meters")
plt.xlabel("Height in cm")
plt.ylabel("Height in meters")
plt.grid(True)
plt.show()
```


    
![png](output_68_0.png)
    


**Explanation**:
- **Height in meters** is perfectly correlated with **Height in centimeters**, with a linear relationship where **1 meter = 100 cm**.
### **3. Low Positive Correlation**

#### **Theory**:
- **Low Positive Correlation** means that there is a weak relationship between the two variables, and the correlation coefficient is between **0** and **1**.

#### **Hypothetical Situation**:
- **Example**: The relationship between **exercise time** and **calories burned**.
  - As people exercise more, they burn more calories, but the effect is weak and not always linear.

#### **Plot and Program**:



```python
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt

# Hypothetical Data: Exercise time vs Calories burned
exercise_time = np.array([1, 2, 3, 4, 5, 6, 7, 8, 9, 10])
calories_burned = exercise_time * 5 + np.random.randint(5, 15, size=10)  # Low positive correlation with noise

# Scatter plot
plt.figure(figsize=(6, 4))
plt.scatter(exercise_time, calories_burned, color='red')
plt.title("Low Positive Correlation: Exercise Time vs Calories Burned")
plt.xlabel("Exercise Time (hours)")
plt.ylabel("Calories Burned")
plt.grid(True)
plt.show()
```


    
![png](output_70_0.png)
    


**Explanation**:
- There is a **weak positive relationship** between **exercise time** and **calories burned**, but with some noise, making the correlation low.

---

### **4. Perfect Negative Correlation**

#### **Theory**:
- **Perfect Negative Correlation** means that as one variable increases, the other decreases in a perfectly linear fashion, with a correlation coefficient of **-1**.

#### **Hypothetical Situation**:
- **Example**: The relationship between **temperature** in Celsius and **ice cream sales**.
  - As the temperature decreases, ice cream sales tend to decrease in a perfectly linear fashion.

#### **Plot and Program**:


```python
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt

# Hypothetical Data: Temperature vs Ice cream sales
temperature = np.array([30, 25, 20, 15, 10, 5, 0])
ice_cream_sales = -temperature + 35  # Perfect negative correlation

# Scatter plot
plt.figure(figsize=(6, 4))
plt.scatter(temperature, ice_cream_sales, color='purple')
plt.title("Perfect Negative Correlation: Temperature vs Ice Cream Sales")
plt.xlabel("Temperature (°C)")
plt.ylabel("Ice Cream Sales")
plt.grid(True)
plt.show()
```


    
![png](output_72_0.png)
    


**Explanation**:
- As **temperature** decreases, **ice cream sales** decrease in a perfectly linear and opposite manner.

---

### **5. High Negative Correlation**

#### **Theory**:
- **High Negative Correlation** means that as one variable increases, the other decreases, and the correlation coefficient is close to **-1**, but not exactly.

#### **Hypothetical Situation**:
- **Example**: The relationship between **time spent watching TV** and **academic performance**.
  - As the time spent watching TV increases, academic performance tends to decrease.

#### **Plot and Program**:



```python
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt

# Hypothetical Data: Time spent watching TV vs Academic performance
tv_time = np.array([1, 2, 3, 4, 5, 6, 7, 8, 9, 10])
academic_performance = -2 * tv_time + 25  # High negative correlation

# Scatter plot
plt.figure(figsize=(6, 4))
plt.scatter(tv_time, academic_performance, color='orange')
plt.title("High Negative Correlation: TV Time vs Academic Performance")
plt.xlabel("TV Time (hours)")
plt.ylabel("Academic Performance")
plt.grid(True)
plt.show()
```


    
![png](output_74_0.png)
    



**Explanation**:
- **TV time** and **academic performance** have a **strong negative relationship**. As one increases, the other decreases.

---

### **6. Low Negative Correlation**

#### **Theory**:
- **Low Negative Correlation** means a weak negative relationship, where the correlation coefficient is between **0** and **-1**.

#### **Hypothetical Situation**:
- **Example**: The relationship between **number of hours spent on social media** and **productivity**.
  - As time spent on social media increases, productivity might decrease, but the relationship is weak.

#### **Plot and Program**:



```python
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt

# Hypothetical Data: Social media time vs Productivity
social_media_time = np.array([1, 2, 3, 4, 5, 6, 7, 8, 9, 10])
productivity = -social_media_time + np.random.randint(0, 5, size=10)  # Low negative correlation with noise

# Scatter plot
plt.figure(figsize=(6, 4))
plt.scatter(social_media_time, productivity, color='pink')
plt.title("Low Negative Correlation: Social Media Time vs Productivity")
plt.xlabel("Social Media Time (hours)")
plt.ylabel("Productivity")
plt.grid(True)
plt.show()
```


    
![png](output_76_0.png)
    


**Explanation**:
- There is a **weak negative correlation** between **social media time** and **productivity**, with some noise.

---

### **7. Null Correlation**

#### **Theory**:
- **Null Correlation** means no relationship between the two variables, and the correlation coefficient is close to **0**.

#### **Hypothetical Situation**:
- **Example**: The relationship between **shoe size** and **IQ**.
  - There is **no relationship** between shoe size and IQ.

#### **Plot and Program**:


```python
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt

# Hypothetical Data: Shoe size vs IQ
shoe_size = np.array([7, 8, 9, 10, 11, 12, 13])
iq = np.array([90, 95, 100, 105, 110, 115, 120])  # No correlation

# Scatter plot
plt.figure(figsize=(6, 4))
plt.scatter(shoe_size, iq, color='yellow')
plt.title("Null Correlation: Shoe Size vs IQ")
plt.xlabel("Shoe Size")
plt.ylabel("IQ")
plt.grid(True)
plt.show()
```


    
![png](output_78_0.png)
    


**Explanation**:
- **Shoe size** and **IQ** have **no relationship**, resulting in a **null correlation**.

---

### **8. U-shape Correlation**

#### **Theory**:
- **U-shape Correlation** indicates that the relationship between two variables forms a U-shape curve, often seen in quadratic relationships.

#### **Hypothetical Situation**:
- **Example**: The relationship between **age** and **happiness**.
  - Happiness may decrease in early adulthood, peak in middle age, and decrease again in older age.

#### **Plot and Program**:



```python
# Hypothetical Data: Age vs Happiness
age = np.array([20, 30, 40, 50, 60])
happiness = np.array([70, 65, 80, 60, 50])  # U-shape relationship

# Scatter plot
plt.figure(figsize=(6, 4))
plt.scatter(age, happiness, color='brown')
plt.title("U-shape Correlation: Age vs Happiness")
plt.xlabel("Age")
plt.ylabel("Happiness")
plt.grid(True)
plt.show()
```


    
![png](output_80_0.png)
    


**Explanation**:
- The relationship forms a **U-shape**, where happiness decreases initially, reaches a peak, and then decreases again.

---

### **9. Exponential Correlation**

#### **Theory**:
- **Exponential Correlation** occurs when one variable changes at an exponential rate in relation to another variable.

#### **Hypothetical Situation**:
- **Example**: The relationship between **investment** and **returns**.
  - As investment increases, returns grow exponentially.

#### **Plot and Program**:



```python
# Hypothetical Data: Investment vs Returns
investment = np.array([100, 200, 300, 400, 500])
returns = np.exp(investment / 100)  # Exponential growth

# Scatter plot
plt.figure(figsize=(6, 4))
plt.scatter(investment, returns, color='green')
plt.title("Exponential Correlation: Investment vs Returns")
plt.xlabel("Investment")
plt.ylabel("Returns")
plt.grid(True)
plt.show()
```


    
![png](output_82_0.png)
    


**Explanation**:
- The relationship between **investment** and **returns** grows **exponentially**, indicating a rapid increase in returns as investment increases.

# Garbage Collection & Memory Optimization

### 1.1 Theory & Concepts

- **Reference Counting**  
  Each object tracks how many references point to it. When refs → 0, Python immediately reclaims its memory.

- **Cycles & Generational GC**  
  Objects in reference cycles (A→B→A) aren’t freed by simple ref-counting. Python’s **cyclic collector** periodically scans “generations” of objects and breaks unreachable cycles.

- **`gc` Module**  
  - `gc.collect()` – force a full collection, returning the number of unreachable objects freed.  
  - `gc.get_threshold()` / `gc.get_count()` – inspect collection thresholds and current counts.

> **Why manually collect?**  
> When working with huge lists/DataFrames, Python may delay cycle cleanup. Calling `gc.collect()` at strategic points ensures memory is reclaimed before further heavy processing.

---

### 1.2 Practical Programs

#### Program 1: Hypothetical Large List Cleanup


```python
import gc, sys

# Create a huge list and check its size
big_list = list(range(20_000_000))
print("Before delete:", sys.getsizeof(big_list), "bytes")

# Remove second half and delete slice
del big_list[10_000_000:]
print("After slice (before GC):", sys.getsizeof(big_list), "bytes")

# Force cycle collector
num_collected = gc.collect()
print("gc.collect() freed objects:", num_collected)
```

    Before delete: 160000056 bytes
    After slice (before GC): 160000056 bytes
    gc.collect() freed objects: 0
    

1. We build a 20 million‐element list.  
2. We delete half, but underlying memory may linger.  
3. `gc.collect()` forces cleanup of any cyclic/unreferenced buffers.

#### Program 2: Hypothetical DataFrame Chunk Processing



```python
import gc
import pandas as pd
import numpy as np

# Simulate streaming chunks of data
def process_chunk(chunk):
    # Dummy transform
    return chunk.applymap(lambda x: x * 2)

# Create a large DataFrame in memory
df = pd.DataFrame(np.random.rand(5000, 2000))
print("Original memory:", df.memory_usage().sum())

# Process in two halves to limit peak memory
mid = len(df) // 2
chunk1 = process_chunk(df.iloc[:mid])
chunk2 = process_chunk(df.iloc[mid:])

# Drop originals and force GC
del df, mid
collected = gc.collect()
print("Objects freed:", collected)

```

    Original memory: 80000132
    

    C:\Users\mrahe\AppData\Local\Temp\ipykernel_20164\2912804789.py:8: FutureWarning:
    
    DataFrame.applymap has been deprecated. Use DataFrame.map instead.
    
    

    Objects freed: 0
    

- Processes data in halves to avoid duplicating the whole DataFrame in memory.  
- Explicit deletion of `df` followed by `gc.collect()` ensures buffers from the original go away.

---

#### Program 3: Cyclic Object Demonstration



```python
import gc

class Node:
    def __init__(self, name):
        self.name = name
        self.next = None

# Create a simple cycle
a = Node('A')
b = Node('B')
a.next = b
b.next = a

# Break local references
del a, b

# At this point, two Node instances form a cycle but have ref‐count > 0.
# Force GC to collect them.
collected = gc.collect()
print("Cyclic nodes collected:", collected)

```

    Cyclic nodes collected: 2
    

- Shows how `gc.collect()` breaks cycles that ref‐counting alone can’t handle.

---

#### Program 4: Titanic Dataset Memory Trim



```python
import gc
import pandas as pd

# 1. Load Titanic data
url = "https://raw.githubusercontent.com/pandas-dev/pandas/master/doc/data/titanic.csv"
df = pd.read_csv(url)
print("Loaded shape:", df.shape)

# 2. Keep only numeric and one-hot encoded columns for modeling
numeric = df.select_dtypes(include='number')
dummies = pd.get_dummies(df[['Sex', 'Embarked']], dummy_na=True)
df_model = pd.concat([numeric, dummies], axis=1)
print("Model shape:", df_model.shape)

# 3. Drop full dataset and force GC
del df, numeric, dummies
freed = gc.collect()
print("Freed objects after cleanup:", freed)

```

    Loaded shape: (891, 12)
    Model shape: (891, 14)
    Freed objects after cleanup: 0
    

- Reads a real dataset, builds a lean modeling frame, then drops the original to reclaim memory immediately.

---

# 2. Data Restructuring (Wide ↔ Long)

### 2.1 Theory & Concepts

- **Wide format**: each subject/ID has multiple variable columns (e.g., sales by quarter).  
- **Long format**: each row is one measurement, with “variable” and “value” columns—preferred by many plotting and statistical libraries.

| Format | Structure                                                         |
|--------|-------------------------------------------------------------------|
| Wide   | `ID | Var1 | Var2 | …`                                            |
| Long   | `ID | Variable | Value`                                          |

- **Key pandas methods**:  
  - **`melt()`**: Wide → Long  
  - **`pivot()`/`pivot_table()`**: Long → Wide (with optional aggregation)  
  - **`stack()`/`unstack()`**: Move index levels into columns and vice versa  

> **When to use**:  
> - For time‐series plots: melt quarterly columns into a single “Quarter” column.  
> - For summary tables: pivot a long survey into a wide question-by-respondent matrix.

---

### 2.2 Practical Programs

#### Program 1: Hypothetical Sales with `.melt()`



```python
import pandas as pd

# Wide: products × quarters
sales_wide = pd.DataFrame({
    'Product': ['X', 'Y', 'Z'],
    'Q1': [120, 200, 340],
    'Q2': [150, 210, 360],
    'Q3': [130, 220, 380],
    'Q4': [160, 230, 400]
})
print("WIDE:\n", sales_wide)

# Melt → Long
sales_long = sales_wide.melt(
    id_vars='Product',
    var_name='Quarter',
    value_name='Sales'
)
print("\nLONG:\n", sales_long)

```

    WIDE:
       Product   Q1   Q2   Q3   Q4
    0       X  120  150  130  160
    1       Y  200  210  220  230
    2       Z  340  360  380  400
    
    LONG:
        Product Quarter  Sales
    0        X      Q1    120
    1        Y      Q1    200
    2        Z      Q1    340
    3        X      Q2    150
    4        Y      Q2    210
    5        Z      Q2    360
    6        X      Q3    130
    7        Y      Q3    220
    8        Z      Q3    380
    9        X      Q4    160
    10       Y      Q4    230
    11       Z      Q4    400
    

- Converts four quarter‐columns into rows, enabling easy quarter‐wise analysis.

---

#### Program 2: Hypothetical Sales Pivot Back & Multiple Aggs



```python
import pandas as pd

# Start from the long version above (sales_long)
# Pivot back to wide, computing both sum and mean (demonstration)
pivot_tbl = sales_long.pivot_table(
    index='Product',
    columns='Quarter',
    values='Sales',
    aggfunc=['sum', 'mean']
)
print("Pivot with sum & mean:\n", pivot_tbl)

```

    Pivot with sum & mean:
              sum                  mean                     
    Quarter   Q1   Q2   Q3   Q4     Q1     Q2     Q3     Q4
    Product                                                
    X        120  150  130  160  120.0  150.0  130.0  160.0
    Y        200  210  220  230  200.0  210.0  220.0  230.0
    Z        340  360  380  400  340.0  360.0  380.0  400.0
    

- Demonstrates `pivot_table()` with multiple aggregation functions, yielding a MultiIndex column.

---

#### Program 3: Titanic Average Fare by Port & Class (`pivot_table`)



```python
import pandas as pd

# Load Titanic data
url = "https://raw.githubusercontent.com/pandas-dev/pandas/master/doc/data/titanic.csv"
df = pd.read_csv(url)

# Wide table: avg fare by embarkation port (rows) and passenger class (cols)
fare_table = df.pivot_table(
    index='Embarked',
    columns='Pclass',
    values='Fare',
    aggfunc='mean'
)
print("Avg Fare (wide):\n", fare_table)

```

    Avg Fare (wide):
     Pclass             1          2          3
    Embarked                                  
    C         104.718529  25.358335  11.214083
    Q          90.000000  12.350000  11.183393
    S          70.364862  20.327439  14.644083
    

- Quickly summarizes numeric data across two categorical dimensions.

---

#### Program 4: Stack & Unstack on Titanic Pivot



```python
# From fare_table above:

# 1. Stack the class-level columns into rows
stacked = fare_table.stack().reset_index()
stacked.columns = ['Embarked', 'Pclass', 'AvgFare']
print("Stacked (long) format):\n", stacked)

# 2. And back to wide with unstack()
unstacked = stacked.set_index(['Embarked','Pclass'])['AvgFare'].unstack()
print("\nUnstacked back to wide:\n", unstacked)

```

    Stacked (long) format):
       Embarked  Pclass     AvgFare
    0        C       1  104.718529
    1        C       2   25.358335
    2        C       3   11.214083
    3        Q       1   90.000000
    4        Q       2   12.350000
    5        Q       3   11.183393
    6        S       1   70.364862
    7        S       2   20.327439
    8        S       3   14.644083
    
    Unstacked back to wide:
     Pclass             1          2          3
    Embarked                                  
    C         104.718529  25.358335  11.214083
    Q          90.000000  12.350000  11.183393
    S          70.364862  20.327439  14.644083
    
