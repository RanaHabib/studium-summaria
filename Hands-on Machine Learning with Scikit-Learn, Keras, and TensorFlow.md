# Hands-on Machine Learning with Scikit-Learn, Keras, and TensorFlow

# Working with Real Data

• Popular open data repositories:
	—UC Irvine Machine Learning Repository
	—Kaggle datasets
	—Amazon’s AWS datasets
• Meta portals (they list open data repositories):
	—http://dataportals.org/
	—http://opendatamonitor.eu/
	—http://quandl.com/
• Other pages listing many popular open data repositories:
	—Wikipedia’s list of Machine Learning datasets
	—Quora.com question
	—Datasets subreddit

# Pipelines

1. Look at the big picture.
2. Get the data.
3. Discover and visualize the data to gain insights.
4. Prepare the data for Machine Learning algorithms.
5. Select a model and train it.
6. Fine-tune your model.
7. Present your solution.
8. Launch, monitor, and maintain your system.

## Look at the Big Picture

### Frame the Problem

**`ask how does the company expect to use and benefit from this model?`**

it will determine:

-  how you frame the problem
- what algorithms you will select
- what performance measure you will use to evaluate your model
- how much effort you should spend tweaking it.

**`ask what the current solution looks like (if any)?`**

It will often give you:

-  a reference performance
- insights on how to solve the problem.

Okay, with all this information you are now ready to start designing your system.
First, you need to frame the problem: is it supervised, unsupervised, or Reinforcement Learning? Is it a classification task, a regression task, or something else? Should you use batch learning or online learning techniques?

`note`

**simple regression**

- **one** y and **one** x `y = f(x)`

**Multiple regression (Multivariable regression)**

- **one** y and **multiple** x `y = f(x1,x2,x3)`

**Multivariate regression**

- **multiple** y and **multiple** x `y1, y2, y3 = f(x1,x2,x3)`

`note`

If the data was huge, you could either split your batch learning work across multiple servers (using the MapReduce technique), or you could use an online learning technique instead.

### Select a Performance Measure

`note`

The higher the norm index, the more it focuses on large values and neglects small ones. This is why the RMSE is more sensitive to outliers than the MAE. But when outliers are exponentially rare (like in a bell-shaped curve), the RMSE performs very well and is generally preferred.

### **Check the Assumptions**

It is good practice to list and verify the assumptions that were made so far, for example, if the system output is going to be fed to a Machine Learning model, and it only outputs (e.g., “cheap,” “medium,” or “expensive”) then you should have worked on the data as a classification task not a regression task.

 You don’t want to find this out after working on a regression system for months.

## Get the Data

### Create the Workspace

### Download the Data

### Take a Quick Look at the Data Structure