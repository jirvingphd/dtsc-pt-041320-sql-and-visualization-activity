
# SQL & Visualization Practice

- Assignment start date: 05/15/20
- Assignment due date: 05/19/20

- onl01-dtsc-pt-041320


## Student Info

- Student Name: 
- Partner Name (if applicable): 



# Instructions:

> - **Your task is to create visualizations to help answer a few question that Northwind, Inc has about its customer's purchasing behaviors.** 
- Each visualization should have a 1-2 sentence explanation about your findings.

   
- **You must select the most appropriate visuals to help answer your question. Options include (but are not limited to):**
    - Scatter plots (color coded by group)
    - Bar plots of group means
    - Boxplots
    - Seaborn barplots, violinplots
    - etc.
    




       
    




- **Read the Visualization Requirements section for additional instructions.**



## Questions

> Question 1: 
 - Does being discounted amount have an effect on the quantity of a product in an order (binary comparison, discount/no discount)? 
 - If so, at what level(s) of discount (multiple-group comparison)?
 
> Question 2: 
 - Does the time of year total Quantities sold? (The time period analyzed is up to you: month,quarter, etc.) 

> Question 3 (Optional):
- Think of one additional question  that you can answer to give Northwind some helpul business insights.

## Visualization Requirements

- **All visualizations (all `fig` objects) should be stored in one dictionary, called `figures` so that they can be displayed together in one final summary cell.**

```python
for question, fig in figures.items():
    print(f"\n\n{question}")
    display(fig)
    
```
- **You must create figures using at least 2 out fo the following ways/approaches to making/starting a figure:**
    1. Use `fig,ax=plt.subplots` to start the figure and then use `ax` to do all of your plotting (e.g. `ax.bar`, `ax.scatter`)
    2. Start a figure with Pandas and then update the axis labels and title outside using the `ax` object that pandas returns combined with `ax.set_` methods.
    3. A Seaborn visualization that takes a whole dataframe and column names to plot(e.g. `sns.barplot(data=df,x='Discount',y="Quantity")`
    4. Use `plt` functions to create a plot and then `plt.gca()` and `plt.gcf()` to get the fig objects.
    
    
- **All visualizations are well labeled with:**
    - axes labels
    - a title
    - and a legend (when appropriate)
    
 

#### Visualization Tips
- Don't forget about our Master Cheat Sheets (all green sheets are plotting-related). 
    - https://drive.google.com/file/d/1PxRAhlaK7ucf0S2F732eJ94ovaPtUSE_/view?usp=sharing
    
    
- Remember that Pandas outputs an `ax` object whenever you use the `df.plot()` method (and most seaborn plots do too).
    - Axes have a `ax.get_figure()` method to get the Figure that goes with an Axes.
    
    
- Remember the 2 special `plt` functions that let us grab the figures and axes we create.
    - `plt.gca()` - get current axis
    - `plt.gcf()` - get current figure
 
 
- Seaborn and pandas both have options for separating your data for you using groups/color. 
    - Some seaborn functions accept a `hue` argument the name of the column to use to color the groups. (`hue='country'`)
    - Some pandas plots accept a similar `c` argument (`c="Discounted"`)
    
    

# SQL Tips/Resources


- The data tables are stored in the `Northwind_small.sqlite` file. 
    - Question 1 uses one table (orderDetail).
    - Questions 2+3 require a join. 
    

### Some SQL tips/reminders

- **To see all tables in a database:**
```python
"""SELECT name FROM sqlite_master WHERE type='table';"""
```

- **To see the information on a table:**
```python
"""PRAGMA table_info(orderDetail)"""
```

    - For more information on Pragma commands: 
        - https://www.sqlite.org/pragma.html
        
        
        
- **Reminder: if a table's name is also a SQL keyword you will have to put quotation marks around the table's name.**

<img src="https://raw.githubusercontent.com/jirvingphd/dsc-mod-3-project-online-ds-ft-100719/master/Northwind_ERD_updated.png">

# Your Work Here


```python
import os
os.listdir()
```


```python
## Import matplotlib, pandas, sqlite3, seaborn

```


```python
## Connect to database with sqlite3
```


```python
## Create the empty figures dictionary for later
figures ={}
```

## Question 1

### Your Work:
- insert as many cells as you need to/would like
- Save the final visual's `Figure` (fig) into the figure dictionary. 


```python

```

### Your Findings/Summary
- 1-2 sentence summary of findings

> ...

## Question 2

### Your Work:
- insert as many cells as you need to/would like
- Save the final visual's `Figure` (fig) into the figure dictionary. 


```python

```

### Your Findings/Summary
- 1-2 sentence summary of findings

> ...

## Question 3 (optional)

### Your Work:
- insert as many cells as you need to/would like
- Save the final visual's `Figure` (fig) into the figure dictionary. 


```python

```

### Your Findings/Summary
- 1-2 sentence summary of findings

> ...

# Final Printout of All Figures


```python
for question, fig in figures.items():
    print(f"\n\n{question}")
    display(fig)
```
