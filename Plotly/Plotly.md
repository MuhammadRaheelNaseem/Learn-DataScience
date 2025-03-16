### **Module 4: Interactive Data Visualizations with Plotly**

---

### **Lecture 1: Introduction to Plotly**

#### **What is Plotly?**
Plotly is a Python library that allows you to create **interactive** and **dynamic** visualizations. Unlike static plots, Plotly charts let users **zoom**, **hover**, and **pan** to explore data in an engaging way. It is used for creating various types of charts such as **scatter plots**, **bar charts**, **3D plots**, and **geographical maps**.

#### **Why Use Plotly?**
1. **Interactivity**: Allows users to interact with plots (hover, zoom, click).
2. **Variety of Plots**: Supports charts like **3D plots**, **heatmaps**, **line plots**, and more.
3. **Easy to Use**: Works well with **Pandas** and **NumPy** for quick data plotting.
4. **Web Integration**: Plots can be shared or embedded in websites.


### **Applications of Plotly:**
- **Business**: Interactive dashboards for sales and performance tracking.
- **Science**: 3D plots for visualizing complex data.
- **Geography**: Mapping regional data on a map.

### **Key Features:**
1. **Interactivity**: Zoom, hover, and explore data.
2. **Customizable**: Change plot appearance and style.
3. **Easy Integration**: Works with Pandas for quick data plotting.


#### **Program 1: Creating an Interactive Scatter Plot for Sales Data**
**Real-World Scenario:** You want to engage stakeholders by visualizing sales data interactively.



```python
import plotly.express as px  # Importing Plotly for interactive plots

# Sample data for sales
data = {'Product': ['A', 'B', 'C', 'D', 'E'],
        'Sales': [200, 300, 400, 500, 600],
        'Region': ['North', 'South', 'East', 'West', 'Central']}  # Sales and regions

# Create a scatter plot
fig = px.scatter(data, x='Product', y='Sales', color='Region', title="Product Sales by Region")  # Scatter plot with color-coded regions
fig.show()  # Display the plot

```

![image](https://github.com/user-attachments/assets/c082f40b-aaf7-4383-8b26-d4ed84d1e365)


**Explanation:** This scatter plot visualizes the sales of different products. By using Plotly, the plot is interactive, allowing users to hover over data points and get more details, improving engagement with stakeholders.

#### **Program 2: Adding Customizable Hover Information**
**Real-World Scenario:** You want to add more details to each data point when hovered.



```python
import plotly.express as px  # Importing Plotly for interactive plots

# Data with more detailed information
data = {'Product': ['A', 'B', 'C', 'D', 'E'],
        'Sales': [200, 300, 400, 500, 600],
        'Region': ['North', 'South', 'East', 'West', 'Central'],
        'Profit': [50, 70, 90, 110, 130]}  # Adding profit data

# Create a scatter plot with hover information
fig = px.scatter(data, x='Product', y='Sales', color='Region', hover_data=['Profit'], title="Product Sales with Profit Info")
fig.show()  # Display the plot

```

![image](https://github.com/user-attachments/assets/f5940e30-a413-4545-8a29-45c80452e801)


**Explanation:** This program customizes the hover information, allowing users to view not only the product name and sales data but also the profit associated with each product when hovering over a data point.

#### **Program 3: Plotting a Bar Chart with Interactive Features**
**Real-World Scenario:** You need to create a bar chart that stakeholders can explore interactively to understand sales across different regions.



```python
import plotly.express as px  # Importing Plotly for interactive charts

# Data for bar chart
data = {'Region': ['North', 'South', 'East', 'West'],
        'Sales': [1000, 1200, 1500, 1300]}

# Create a bar chart
fig = px.bar(data, x='Region', y='Sales', title="Sales by Region", labels={'Sales': 'Total Sales ($)', 'Region': 'Region Name'})
fig.show()  # Display the plot
```

![image](https://github.com/user-attachments/assets/b5eebc5b-0857-47c8-b8b8-206bf59edde1)

**Explanation:** This bar chart allows users to interactively explore the sales data across different regions. Plotly’s interactive features, such as zooming and tooltips, help users engage with the data effectively.

#### **Program 4: Customizing Plot Appearance with Plotly**
**Real-World Scenario:** You want to create a visually appealing chart for a report with customized colors and styles.



```python
import plotly.express as px  # Importing Plotly for customizing charts

# Sample sales data
data = {'Product': ['A', 'B', 'C', 'D'],
        'Sales': [250, 400, 350, 500]}

# Create a bar chart with customized colors
fig = px.bar(data, x='Product', y='Sales', title="Sales by Product", color='Sales', color_continuous_scale='Viridis')
fig.show()  # Display the plot
```

![image](https://github.com/user-attachments/assets/c17e4e9c-375a-44b1-a43a-da5e24c54ec6)

**Explanation:** This bar chart uses the ‘Viridis’ color scale, making the chart visually appealing while representing the sales data. The color of the bars changes according to the sales value, helping users interpret the data more easily.

#### **Program 5: Real-World Scenario – Interactive Plot for Yearly Sales**
**Real-World Scenario:** You want to display yearly sales growth interactively for a financial presentation.



```python
import plotly.express as px  # Importing Plotly for interactive plots

# Data for yearly sales
data = {'Year': [2019, 2020, 2021, 2022],
        'Sales': [10000, 15000, 20000, 25000]}

# Create an interactive line plot for yearly sales
fig = px.line(data, x='Year', y='Sales', title="Yearly Sales Growth")
fig.show()  # Display the plot

```

![image](https://github.com/user-attachments/assets/538cd03c-0d09-4709-bffe-ff389e7b4cbb)

**Explanation:** The line plot here shows the sales growth over the years. It’s interactive, so users can hover over points to get detailed information, making it ideal for engaging stakeholders in a presentation.


---

### **Lecture 2: 3D Visualizations with Plotly**

#### **Program 1: 3D Scatter Plot for Sales Across Multiple Regions**
**Real-World Scenario:** You want to visualize sales data across multiple regions and products in 3D.



```python
import plotly.express as px  # Importing Plotly for 3D plots

# 3D data for sales
data = {'Product': ['A', 'B', 'C', 'D', 'E'],
        'Sales': [200, 300, 400, 500, 600],
        'Profit': [50, 70, 90, 110, 130],
        'Region': ['North', 'South', 'East', 'West', 'Central']}

# Create a 3D scatter plot
fig = px.scatter_3d(data, x='Product', y='Sales', z='Profit', color='Region', title="3D Sales and Profit Data")
fig.show()  # Display the plot

```

![image](https://github.com/user-attachments/assets/a3d7bef0-7c72-42da-972c-1a4ef2c8c0f1)

**Explanation:** This 3D scatter plot visualizes sales, profit, and region data in three dimensions, making it easier to understand the relationships between these factors interactively.

#### **Program 2: 3D Surface Plot for Sales Over Time**
**Real-World Scenario:** You need to visualize sales over time and regions in a 3D space.



```python
import plotly.graph_objects as go  # Importing Plotly for advanced 3D plots

# Data for surface plot
data = {'Months': ['Jan', 'Feb', 'Mar', 'Apr'],
        'Regions': ['North', 'South', 'East', 'West'],
        'Sales': [[200, 220, 240, 260], [280, 300, 320, 340], [350, 370, 390, 410], [420, 440, 460, 480]]}

# Create a 3D surface plot
fig = go.Figure(data=[go.Surface(z=data['Sales'], x=data['Months'], y=data['Regions'])])
fig.update_layout(title='3D Surface Plot for Sales by Region and Month')
fig.show()  # Display the plot

```

![image](https://github.com/user-attachments/assets/cbedc6d4-a8df-4725-b953-7c53de4f68b4)

**Explanation:** This 3D surface plot visualizes sales data over multiple months and regions. It helps users understand the variation in sales more intuitively by adding a third dimension (surface plot).

#### **Program 3: Real-World Scenario – Product and Sales Interaction in 3D**
**Real-World Scenario:** Visualize product sales and marketing spend across time and regions.



```python
import plotly.graph_objects as go  # Importing Plotly for 3D plot creation

# Data for product sales and marketing spend
product_data = {'Months': ['Jan', 'Feb', 'Mar', 'Apr'],
                'Regions': ['North', 'South', 'East', 'West'],
                'Sales': [[200, 220, 240, 260], [280, 300, 320, 340], [350, 370, 390, 410], [420, 440, 460, 480]]}

# Create a 3D scatter plot
fig = go.Figure(data=[go.Scatter3d(x=product_data['Months'], y=product_data['Regions'], z=product_data['Sales'])])
fig.update_layout(title="Sales and Marketing Interaction in 3D")
fig.show()  # Display the plot

```

![image](https://github.com/user-attachments/assets/1fcbaf99-3920-48ad-b7eb-4e8627db2dd5)


**Explanation:** This 3D scatter plot visualizes the interaction between product sales and marketing efforts, helping in understanding how both factors influence each other over time.


#### **Program 4: Creating a 3D Line Plot for Product Growth**
**Real-World Scenario:** Visualize the growth of different product sales over time and region.


```python
import plotly.graph_objects as go  # Importing Plotly for advanced 3D plotting

# Data for product growth
products = ['A', 'B', 'C', 'D']
regions = ['North', 'South', 'East', 'West']
sales_growth = [[100, 200, 300, 400], [150, 250, 350, 450], [200, 300, 400, 500], [250, 350, 450, 550]]

# Create a 3D line plot
fig = go.Figure(data=[go.Scatter3d(x=products, y=regions, z=sales_growth)])
fig.update_layout(title="Product Sales Growth in 3D")
fig.show()  # Display the plot
```

![image](https://github.com/user-attachments/assets/75ed4101-d38a-428d-8df6-bd98a79b5377)

**Explanation:** This 3D line plot visualizes the growth of product sales, helping users visualize data across multiple dimensions of product, region, and sales performance.


#### **Program 5: Visualizing Multiple Dimensions in 3D for Product Data**
**Real-World Scenario:** You want to analyze how products perform across different regions and sales channels.


```python
import plotly.graph_objects as go  # Importing Plotly for advanced 3D plotting

# Product performance data
products = ['A', 'B', 'C', 'D']
regions = ['North', 'South', 'East', 'West']
sales = [[100, 200, 300, 400], [150, 250, 350, 450], [200, 300, 400, 500], [250, 350, 450, 550]]

# Create a 3D surface plot for product data
fig = go.Figure(data=[go.Surface(z=sales, x=products, y=regions)])
fig.update_layout(title="Product Data Performance in 3D")
fig.show()  # Display the plot
```

![image](https://github.com/user-attachments/assets/430ad747-bfd5-499f-9709-322cafeae6a2)

**Explanation:** This 3D surface plot visualizes how products perform across different regions and sales figures, helping businesses make more informed decisions about their product strategies.

---

### **Lecture 3: Geographic Data Visualization with Plotly**

#### **Program 1: Creating a Choropleth Map for Regional Sales**
**Real-World Scenario:** You need to show regional sales performance on a map.



```python
import plotly.express as px  # Importing Plotly for geo plotting

# Data for regional sales
data = {'Region': ['North', 'South', 'East', 'West'],
        'Sales': [5000, 7000, 8000, 6000]}

# Create a choropleth map
fig = px.choropleth(data, locations='Region', color='Sales', hover_name='Region', color_continuous_scale='Viridis')
fig.update_layout(title='Regional Sales Performance')
fig.show()  # Display the map

```

![image](https://github.com/user-attachments/assets/d9e02e6c-0f12-42fa-a5bc-17e4234a0e10)

**Explanation:** This choropleth map shows the sales performance for different regions, color-coded for better comparison.


#### **Program 2: Plotting a Geographic Heatmap for Sales**
**Real-World Scenario:** You need to visualize sales density across different geographical areas.


```python
import pandas as pd
import plotly.express as px

# Data for geographic heatmap
data = {
    'Latitude': [40.7128, 34.0522, 51.5074, 48.8566],
    'Longitude': [-74.0060, -118.2437, -0.1278, 2.3522],
    'Sales': [2000, 1500, 1800, 2200]
}

# Convert dictionary to a Pandas DataFrame
df = pd.DataFrame(data)

# --- Option 1: Density Mapbox ---
# Create a geographic density mapbox for Sales
fig = px.density_mapbox(
    df,
    lat='Latitude',
    lon='Longitude',
    z='Sales',
    radius=10,
    color_continuous_scale='YlGnBu'
)

# Update layout: set the map style, title, center, and zoom level
fig.update_layout(
    mapbox_style="carto-positron",
    title="Sales Density Heatmap",
    mapbox=dict(
        center=dict(lat=45, lon=0),  # Adjust center as needed
        zoom=1                     # Adjust zoom level for a global view
    )
)

fig.show()

# --- Option 2: Scatter Mapbox ---
# If the density map appears too gray due to few points,
# a scatter map can be used to clearly show each data point.
fig2 = px.scatter_mapbox(
    df,
    lat='Latitude',
    lon='Longitude',
    size='Sales',               # Marker size reflects Sales value
    color='Sales',              # Marker color reflects Sales value
    color_continuous_scale='YlGnBu',
    size_max=15,
    zoom=1,
    title="Sales Scatter Map"
)

# Use the same map style for consistency
fig2.update_layout(mapbox_style="carto-positron")

fig2.show()
```

![image](https://github.com/user-attachments/assets/bee8e713-bc29-4a67-b95b-4b18335f5be3)
![image](https://github.com/user-attachments/assets/f4b7e5b1-2661-4b50-8d58-fb9d27cb7658)


**Explanation:** The density map visualizes the geographical distribution of sales across various cities, giving a clear idea of where sales are more concentrated.

#### **Program 3: Visualizing Regional Sales with a Geo Scatter Plot**
**Real-World Scenario:** You want to display the geographical distribution of sales data points.



```python
import plotly.express as px  # Importing Plotly for geo plotting

# Data for sales points in various regions
data = {'Latitude': [40.7128, 34.0522, 51.5074, 48.8566],
        'Longitude': [-74.0060, -118.2437, -0.1278, 2.3522],
        'Sales': [2000, 1500, 1800, 2200]}  # Sales values for cities

# Create a geo scatter plot
fig = px.scatter_geo(data, lat='Latitude', lon='Longitude', size='Sales', title="Geographic Distribution of Sales")
fig.show()  # Display the plot

```

![image](https://github.com/user-attachments/assets/b83a674b-fe44-44f5-9177-b49f0aa61bc1)


**Explanation:** This geo scatter plot places data points on a map according to their latitude and longitude, with the size of each point reflecting sales volume.

#### **Program 4: Visualizing Sales Data by Region on a World Map**
**Real-World Scenario:** You want to show how sales are performing worldwide by region.



```python
import plotly.express as px  # Importing Plotly for geo plotting

# Global sales data
data = {'Region': ['North America', 'Europe', 'Asia', 'Africa'],
        'Sales': [10000, 15000, 20000, 5000]}

# Create a choropleth map for global sales
fig = px.choropleth(data, locations='Region', color='Sales', hover_name='Region', color_continuous_scale='Blues')
fig.update_layout(title="Global Sales by Region")
fig.show()  # Display the map
```

![image](https://github.com/user-attachments/assets/09ad411d-33c5-4ac8-ab85-0333139fdb2c)

**Explanation:** This map visualizes sales data for different regions of the world, helping stakeholders see global performance at a glance.


#### **Program 5: Real-World Scenario – Sales Performance in Different Countries**
**Real-World Scenario:** You want to visualize how sales vary in different countries.


```python
import plotly.express as px  # Importing Plotly for geo plotting

# Country sales data
data = {'Country': ['USA', 'Canada', 'Germany', 'UK'],
        'Sales': [25000, 20000, 30000, 15000]}

# Create a choropleth map for sales performance by country
fig = px.choropleth(data, locations='Country', color='Sales', hover_name='Country', color_continuous_scale='YlOrRd')
fig.update_layout(title="Sales Performance by Country")
fig.show()  # Display the map
```

![image](https://github.com/user-attachments/assets/52607381-e3a9-4557-a1e4-8bc64778a03b)

**Explanation:** This choropleth map shows sales data by country, using color scales to represent sales performance.


---

### **Lecture 4: Advanced Plotly Features for Interactive Dashboards**

#### **Program 1: Creating a Gauge Chart for Sales Performance**
**Real-World Scenario:** You need to visualize how close your sales are to your target using a gauge chart.



```python
import plotly.graph_objects as go  # Importing Plotly for advanced chart types

# Sales data
sales = 75  # Percentage of sales target achieved
target = 100  # Target sales

# Create a gauge chart
fig = go.Figure(go.Indicator(
    mode="gauge+number", 
    value=sales, 
    title={'text': "Sales Performance"}, 
    gauge={'axis': {'range': [0, target]}, 'bar': {'color': "green"}}))
fig.show()  # Display the chart
```

![image](https://github.com/user-attachments/assets/8460e4a7-2aa3-4a92-9c6f-2f2df485bffc)


**Explanation:** This gauge chart shows how much of the sales target has been achieved. It’s interactive, so users can explore the percentage visually.

#### **Program 2: Adding Interactive Dropdown for Data Filtering**
**Real-World Scenario:** You want to allow users to filter sales data interactively using a dropdown menu.



```python
import plotly.express as px  # Importing Plotly for interactive plots

# Data for sales by product
data = {'Product': ['A', 'B', 'C', 'D'],
        'Sales': [250, 400, 350, 500],
        'Region': ['North', 'South', 'East', 'West']}

# Create a bar chart
fig = px.bar(data, x='Product', y='Sales', color='Region', title="Sales by Product")

# Add a dropdown for filtering regions
fig.update_layout(
    updatemenus=[{
        'buttons': [
            {'label': 'All', 'method': 'update', 'args': [{'visible': [True, True, True, True]}, {'title': 'Sales by Product'}]},
            {'label': 'North', 'method': 'update', 'args': [{'visible': [True, False, False, False]}, {'title': 'Sales in North'}]},
            {'label': 'South', 'method': 'update', 'args': [{'visible': [False, True, False, False]}, {'title': 'Sales in South'}]},
            {'label': 'East', 'method': 'update', 'args': [{'visible': [False, False, True, False]}, {'title': 'Sales in East'}]},
            {'label': 'West', 'method': 'update', 'args': [{'visible': [False, False, False, True]}, {'title': 'Sales in West'}]}
        ],
        'direction': 'down',
        'showactive': True,
    }]
)
fig.show()  # Display the plot

```

![image](https://github.com/user-attachments/assets/a8e840f9-8d9b-4181-af4a-eb156dcdc284)


**Explanation:** This interactive bar chart allows users to filter the sales data by region using a dropdown menu, enhancing data exploration.

#### **Program 3: Real-Time Interactive Line Chart for Sales Trends**
**Real-World Scenario:** Visualize sales trends in real-time to monitor performance over time.


```python
import plotly.graph_objects as go  # Importing Plotly for advanced plotting

# Time series data for sales trends
months = ['Jan', 'Feb', 'Mar', 'Apr', 'May']
sales = [200, 220, 240, 260, 280]

# Create an interactive line chart for sales trends
fig = go.Figure(go.Scatter(x=months, y=sales, mode='lines+markers', name='Sales Trend'))
fig.update_layout(title="Real-Time Sales Trends", xaxis_title="Month", yaxis_title="Sales ($)")
fig.show()  # Display the plot
```

![image](https://github.com/user-attachments/assets/41402a0e-6034-4636-a336-59dcade32c58)

**Explanation:** This line chart visualizes the sales trend over time and allows users to interactively explore how sales evolve month by month.

#### **Program 4: Creating a Donut Chart for Market Share**
**Real-World Scenario:** Visualize market share among different companies using an interactive donut chart.


```python
import plotly.graph_objects as go  # Importing Plotly for advanced chart types

# Market share data
labels = ['Company A', 'Company B', 'Company C', 'Company D']
values = [50, 30, 10, 10]

# Create a donut chart
fig = go.Figure(go.Pie(labels=labels, values=values, hole=0.3))
fig.update_layout(title="Market Share Distribution")
fig.show()  # Display the plot

```
![image](https://github.com/user-attachments/assets/3dcc4c96-726a-4f59-a395-9be1f741a050)

**Explanation:** The donut chart helps visualize market share in an interactive and visually appealing way.

#### **Program 5: Real-World Scenario – Interactive Financial Dashboard**
**Real-World Scenario:** You want to create an interactive dashboard showing different financial metrics.


```python
import plotly.express as px  # Importing Plotly for dashboard creation

# Data for financial metrics
data = {'Metric': ['Revenue', 'Expenses', 'Profit'],
        'Value': [50000, 30000, 20000]}

# Create a pie chart for financial data
fig = px.pie(data, names='Metric', values='Value', title='Financial Breakdown')
fig.show()  # Display the plot
```
![image](https://github.com/user-attachments/assets/e882cd3e-6d90-41e0-bbb8-f2e2e075c83e)

**Explanation:** This interactive dashboard visualizes key financial metrics, making it easy for stakeholders to explore the breakdown of revenue, expenses, and profit.

---

### **Lecture 5: Customizing and Enhancing Plots with Plotly**

#### **Program 1: Customizing Bar Chart with Interactive Hover Features**
**Real-World Scenario:** Customize a bar chart with interactive hover features to display more detailed information.


```python
import plotly.express as px  # Importing Plotly for interactive charts

# Data for the bar chart
data = {'Product': ['A', 'B', 'C', 'D'],
        'Sales': [250, 400, 350, 500]}

# Create a bar chart with hover features
fig = px.bar(data, x='Product', y='Sales', title="Sales by Product", 
             hover_data={'Product': True, 'Sales': True})
fig.show()  # Display the plot
```

![image](https://github.com/user-attachments/assets/ea418482-db8e-4675-bee7-3ed613a49b7b)

**Explanation:** This bar chart includes hover functionality, so users can view product names and sales figures in more detail when hovering over the bars.


#### **Program 2: Adding Custom Shapes to Enhance Plot Appearance**
**Real-World Scenario:** Enhance the visual appeal of a plot by adding custom shapes, such as lines or markers.


```python
import plotly.graph_objects as go  # Importing Plotly for advanced chart types

# Data for sales
months = ['Jan', 'Feb', 'Mar', 'Apr']
sales = [200, 250, 300, 350]

# Create a line chart
fig = go.Figure(go.Scatter(x=months, y=sales, mode='lines+markers', name='Sales'))

# Add a custom line to the plot
fig.add_shape(type='line', x0=0, y0=200, x1=3, y1=350, line=dict(color='Red', width=3))  # Adding a line
fig.show()  # Display the plot
```

![image](https://github.com/user-attachments/assets/24fcf8dd-2019-40d0-ab2f-93ebe23a4f4e)

**Explanation:** This program enhances the plot with custom shapes, such as adding a red line to highlight trends or specific data points.


#### **Program 3: Customizing Plot Annotations for Clarity**
**Real-World Scenario:** Add annotations to a plot for better understanding and clarification of key points.


```python
import plotly.graph_objects as go  # Importing Plotly for advanced charts

# Data for the plot
months = ['Jan', 'Feb', 'Mar', 'Apr']
sales = [200, 250, 300, 350]

# Create the plot
fig = go.Figure(go.Scatter(x=months, y=sales, mode='lines+markers'))

# Add annotation for a key data point
fig.add_annotation(x=2, y=300, text="Peak Sales", showarrow=True, arrowhead=2, arrowsize=1)
fig.show()  # Display the plot
```

![image](https://github.com/user-attachments/assets/cc8af0fa-fd3e-429e-b9e9-f696120bf24d)

**Explanation:** An annotation is added to mark the "Peak Sales" point in the plot, making it easier to highlight significant data points.


#### **Program 4: Real-World Scenario – Stock Price Visualization**
**Real-World Scenario:** Visualize stock prices with interactive features to engage investors and analysts.



```python
import plotly.graph_objects as go  # Importing Plotly for creating plots

# Data for stock prices
dates = ['2022-01-01', '2022-01-02', '2022-01-03', '2022-01-04']
prices = [100, 105, 110, 115]

# Create an interactive line chart for stock prices
fig = go.Figure(go.Scatter(x=dates, y=prices, mode='lines+markers', name='Stock Price'))
fig.update_layout(title="Stock Price Over Time", xaxis_title="Date", yaxis_title="Price ($)")
fig.show()  # Display the plot
```

![image](https://github.com/user-attachments/assets/94ccd34b-770e-4fb1-91a3-bcf539104893)

**Explanation:** This plot helps visualize stock price changes over time with interactive features, allowing users to explore the data in more detail.

#### **Program 5: Creating a Customizable Interactive Dashboard for Data Analytics**
**Real-World Scenario:** Build an interactive dashboard to monitor key business metrics such as revenue, sales, and profits.



```python
import plotly.graph_objects as go  # Importing Plotly for advanced plotting

# Data for dashboard
metrics = ['Revenue', 'Sales', 'Profit']
values = [50000, 35000, 15000]

# Create a pie chart for the dashboard
fig = go.Figure(data=[go.Pie(labels=metrics, values=values)])
fig.update_layout(title="Business Dashboard")
fig.show()  # Display the plot
```

![image](https://github.com/user-attachments/assets/3c864e31-bb89-483d-abcf-593760116829)

**Explanation:** This interactive dashboard allows users to monitor business metrics like revenue, sales, and profits at a glance.

---

### **Lecture 6: Plotly with Pandas for Data Analysis**

#### **Program 1: Plotting Sales Data from a Pandas DataFrame**
**Real-World Scenario:** Visualize sales data from a Pandas DataFrame.


```python
import plotly.express as px  # Importing Plotly for interactive plotting
import pandas as pd  # Importing Pandas for data manipulation

# Sample sales data
data = {'Product': ['A', 'B', 'C', 'D'],
        'Sales': [250, 400, 350, 500]}
df = pd.DataFrame(data)  # Creating a DataFrame

# Create a bar plot from the DataFrame
fig = px.bar(df, x='Product', y='Sales', title="Sales by Product")
fig.show()  # Display the plot
```

![image](https://github.com/user-attachments/assets/c58c5b9b-53c2-46e9-aab5-273890cba136)

**Explanation:** This program shows how to plot sales data from a Pandas DataFrame using Plotly, making data analysis more efficient.


#### **Program 2: Plotting a Time Series from a DataFrame**
**Real-World Scenario:** Visualize time series data for sales growth over time.


```python
import plotly.express as px  # Importing Plotly for plotting
import pandas as pd  # Importing Pandas for data manipulation

# Time series data
data = {'Date': pd.date_range(start='2022-01-01', periods=5, freq='ME'),
        'Sales': [1000, 1200, 1500, 1800, 2100]}
df = pd.DataFrame(data)  # Creating a DataFrame

# Create a line plot for sales growth over time
fig = px.line(df, x='Date', y='Sales', title="Sales Growth Over Time")
fig.show()  # Display the plot
```

![image](https://github.com/user-attachments/assets/96093211-7e05-40d0-a23d-3f57b2935bad)

**Explanation:** This line plot visualizes sales data over time, allowing users to analyze trends and growth in a time series format.

#### **Program 3: Real-World Scenario – Correlation Matrix from DataFrame**
**Real-World Scenario:** Visualize the correlation between various business metrics.


```python
import plotly.express as px  # Importing Plotly for plotting
import pandas as pd  # Importing Pandas for data manipulation

# Sample data
data = {'Sales': [100, 200, 300, 400, 500],
        'Profit': [20, 40, 60, 80, 100],
        'Expenses': [50, 60, 70, 80, 90]}
df = pd.DataFrame(data)  # Creating a DataFrame

# Create a heatmap for correlation matrix
fig = px.imshow(df.corr(), text_auto=True, title="Correlation Matrix")
fig.show()  # Display the plot
```

![image](https://github.com/user-attachments/assets/0667822f-d704-466e-8681-5ec7c1a56e71)

**Explanation:** This heatmap visualizes the correlation between sales, profit, and expenses, allowing users to understand the relationships between different metrics.


#### **Program 4: Grouped Bar Plot from a Pandas DataFrame**
**Real-World Scenario:** Visualize sales data by region using a grouped bar chart.


```python
import plotly.express as px  # Importing Plotly for plotting
import pandas as pd  # Importing Pandas for data manipulation

# Sample data
data = {'Region': ['North', 'South', 'East', 'West'],
        'Sales': [1000, 1500, 2000, 2500],
        'Profit': [200, 300, 400, 500]}
df = pd.DataFrame(data)  # Creating a DataFrame

# Create a grouped bar plot
fig = px.bar(df, x='Region', y=['Sales', 'Profit'], title="Sales and Profit by Region")
fig.show()  # Display the plot
```

![image](https://github.com/user-attachments/assets/c9f46932-4d1f-47ea-a82d-04748c0ca9b9)


**Explanation:** This grouped bar chart helps visualize both sales and profit data side-by-side, making it easier to compare the performance by region.


---

### **Lecture 7: Advanced Geographic Plotting and Interactive Dashboards**

#### **Program 1: 3D Geographic Visualization for Sales Across Locations**
**Real-World Scenario:** Visualize sales across different geographical locations in 3D.


```python
import plotly.graph_objects as go  # Importing Plotly for 3D plots

# Sample data for 3D geographic plotting
locations = ['New York', 'Los Angeles', 'Chicago']
latitudes = [40.7128, 34.0522, 41.8781]
longitudes = [-74.0060, -118.2437, -87.6298]
sales = [5000, 7000, 6000]

# Create a 3D scatter plot for geographic data
fig = go.Figure(go.Scattergeo(
    locationmode='USA-states',  # Geographic mode for USA
    lon=longitudes, lat=latitudes, text=locations, marker=dict(size=12, color=sales, colorscale='Viridis', showscale=True)
))
fig.update_layout(title="3D Geographic Visualization of Sales")
fig.show()  # Display the plot

```
![image](https://github.com/user-attachments/assets/69b1bbd0-d2f2-42e2-a20f-19e42134a51b)

**Explanation:** This 3D plot visualizes sales data across different locations, helping users explore the geographic spread of sales.

#### **Program 2: Creating a Custom Dashboard with Plotly Dash**
**Real-World Scenario:** You want to create a full interactive dashboard to track and analyze business metrics.



```python
pip install dash
```

```output
Requirement already satisfied: dash in c:\users\mrahe\anaconda3\lib\site-packages (2.18.2)Note: you may need to restart the kernel to use updated packages.

Requirement already satisfied: Flask<3.1,>=1.0.4 in c:\users\mrahe\anaconda3\lib\site-packages (from dash) (3.0.3)
Requirement already satisfied: Werkzeug<3.1 in c:\users\mrahe\anaconda3\lib\site-packages (from dash) (3.0.3)
Requirement already satisfied: plotly>=5.0.0 in c:\users\mrahe\anaconda3\lib\site-packages (from dash) (5.24.1)
Requirement already satisfied: dash-html-components==2.0.0 in c:\users\mrahe\anaconda3\lib\site-packages (from dash) (2.0.0)
Requirement already satisfied: dash-core-components==2.0.0 in c:\users\mrahe\anaconda3\lib\site-packages (from dash) (2.0.0)
Requirement already satisfied: dash-table==5.0.0 in c:\users\mrahe\anaconda3\lib\site-packages (from dash) (5.0.0)
Requirement already satisfied: importlib-metadata in c:\users\mrahe\anaconda3\lib\site-packages (from dash) (7.0.1)
Requirement already satisfied: typing-extensions>=4.1.1 in c:\users\mrahe\anaconda3\lib\site-packages (from dash) (4.11.0)
Requirement already satisfied: requests in c:\users\mrahe\anaconda3\lib\site-packages (from dash) (2.32.3)
Requirement already satisfied: retrying in c:\users\mrahe\anaconda3\lib\site-packages (from dash) (1.3.4)
Requirement already satisfied: nest-asyncio in c:\users\mrahe\anaconda3\lib\site-packages (from dash) (1.6.0)
Requirement already satisfied: setuptools in c:\users\mrahe\anaconda3\lib\site-packages (from dash) (75.1.0)
Requirement already satisfied: Jinja2>=3.1.2 in c:\users\mrahe\anaconda3\lib\site-packages (from Flask<3.1,>=1.0.4->dash) (3.1.4)
Requirement already satisfied: itsdangerous>=2.1.2 in c:\users\mrahe\anaconda3\lib\site-packages (from Flask<3.1,>=1.0.4->dash) (2.2.0)
Requirement already satisfied: click>=8.1.3 in c:\users\mrahe\anaconda3\lib\site-packages (from Flask<3.1,>=1.0.4->dash) (8.1.7)
Requirement already satisfied: blinker>=1.6.2 in c:\users\mrahe\anaconda3\lib\site-packages (from Flask<3.1,>=1.0.4->dash) (1.6.2)
Requirement already satisfied: tenacity>=6.2.0 in c:\users\mrahe\anaconda3\lib\site-packages (from plotly>=5.0.0->dash) (8.2.3)
Requirement already satisfied: packaging in c:\users\mrahe\anaconda3\lib\site-packages (from plotly>=5.0.0->dash) (24.1)
Requirement already satisfied: MarkupSafe>=2.1.1 in c:\users\mrahe\anaconda3\lib\site-packages (from Werkzeug<3.1->dash) (2.1.3)
Requirement already satisfied: zipp>=0.5 in c:\users\mrahe\anaconda3\lib\site-packages (from importlib-metadata->dash) (3.17.0)
Requirement already satisfied: charset-normalizer<4,>=2 in c:\users\mrahe\anaconda3\lib\site-packages (from requests->dash) (3.3.2)
Requirement already satisfied: idna<4,>=2.5 in c:\users\mrahe\anaconda3\lib\site-packages (from requests->dash) (3.7)
Requirement already satisfied: urllib3<3,>=1.21.1 in c:\users\mrahe\anaconda3\lib\site-packages (from requests->dash) (2.2.3)
Requirement already satisfied: certifi>=2017.4.17 in c:\users\mrahe\anaconda3\lib\site-packages (from requests->dash) (2024.8.30)
Requirement already satisfied: six>=1.7.0 in c:\users\mrahe\anaconda3\lib\site-packages (from retrying->dash) (1.16.0)
Requirement already satisfied: colorama in c:\users\mrahe\anaconda3\lib\site-packages (from click>=8.1.3->Flask<3.1,>=1.0.4->dash) (0.4.6)
```

```python
import dash
import dash_core_components as dcc
import dash_html_components as html
import plotly.graph_objs as go

# Initialize the Dash app
app = dash.Dash()

# Create a simple layout with a graph
app.layout = html.Div([
    dcc.Graph(
        id='sales-graph',
        figure={
            'data': [
                go.Bar(x=['Jan', 'Feb', 'Mar'], y=[1000, 1500, 2000])
            ],
            'layout': go.Layout(
                title='Sales by Month'
            )
        }
    )
])

# Run the app
if __name__ == '__main__':
    app.run_server(debug=True)

```

![image](https://github.com/user-attachments/assets/b8a3990a-34c5-41ef-b350-844371f8cc0e)

**Explanation:** This simple **Dash** app creates an interactive web-based dashboard displaying sales data by month.
