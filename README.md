![Logo

Description automatically generated](Aspose.Words.b27983c4-86a6-4da3-a49b-920ee8887e99.001.jpeg)

**DATA 1202 – Data Analysis Tools

Assignment #4

Group : 2**

Student Names – Navneet Singh, Diksha Kumawat, Ketki Jagtap, Karandeep Singh


Submitted to: Professor Omar

Submitted On: 15/07/2022








**Dataset used:** youtube\_dataset.csv

- An extraction of the top 4000 YouTube channels based on Subscribers. 

**1. Create a function to calculate the distribution of channel type from the top 1000 records.**

\# Function to calculate the distribution of channel type from the top 1000 records

def subset\_data\_channeltype\_distribution(df, no\_of\_rows):

`  `subset = df.head(no\_of\_rows)

`  `return subset.groupby('channeltype')['channeltype'].count()

subset\_data\_channeltype\_distribution(data,1000)

` `# passing number of rows as a variable to make the function dynamic

**Output:**

![](Aspose.Words.b27983c4-86a6-4da3-a49b-920ee8887e99.002.png)

**Syntax for Function:**

def function\_name(parameters):

`	`"""docstring"""

`	  `statement(s)

**Explanation of our Function**:

def subset\_data\_channeltype\_distribution(df, no\_of\_rows):

In this keyword def is used to define a function. The function that we have created is subset\_data\_channeltype\_distribution. The text inside the round bracket are the parameters of the function through which we pass values to the function. The parameters we are passing to our function, subset\_data\_channeltype\_distribution, is df and no of rows.

subset = df.head(no\_of\_rows)

This statement is the part of the body of a function. Here we are simply defining the value of subset to be the no of rows.

return subset.groupby('channeltype')['channeltype'].count()

In this returns statement we are sending the result of function back to the caller. Our return statement will send the values channel type and its count when called.

subset\_data\_channeltype\_distribution(data,1000)

This is our function call statement while calling it we are passing the values data and 1000 to make the function dynamic. Here data is our csv file and 1000 would mean the top 1000 records of it.

So basically, our function will evaluate top 1000 records of the csv file based on their channel type and give the count of each channel type.

**2. Load only the top 1000 records of the original 4000 into a separate CSV file, and to a database table.** 

#Top 1000 records inserted into a CSV file named youtube\_dataset\_top\_1000\_rows.csv

subset\_data\_frame = data.head(1000)

subset\_data\_frame.to\_csv("youtube\_dataset\_top\_1000\_rows.csv")

Here we have assigned the top 1000 records of our original csv file to subset\_data\_frame.

The second statement is used to convert this data to a csv file using a .to\_csv() extention.

The new csv file is called as "youtube\_dataset\_top\_1000\_rows.csv".

![](Aspose.Words.b27983c4-86a6-4da3-a49b-920ee8887e99.003.png)

![](Aspose.Words.b27983c4-86a6-4da3-a49b-920ee8887e99.004.png)

Next we have imported this file on to a database and run a select command to view the results.

![](Aspose.Words.b27983c4-86a6-4da3-a49b-920ee8887e99.005.png)

`  `**![](Aspose.Words.b27983c4-86a6-4da3-a49b-920ee8887e99.006.png)**

![](Aspose.Words.b27983c4-86a6-4da3-a49b-920ee8887e99.007.png)

![](Aspose.Words.b27983c4-86a6-4da3-a49b-920ee8887e99.008.png)LOG OF STUDENT’S CONTRIBUTION:


|Tasks|Participants|
| :-: | :-: |
|Arrange a call to discuss the assignment and allocate the tasks. |Navneet Singh, Ketki Jagtap, Diksha Kumawat, Karandeep Singh|
|Create a function |Navneet Singh, Ketki Jagtap|
|Create a query to Load only the top 1000 records and run Select command.|Diksha Kumawat, Karandeep Singh|
|Making the query more efficient|Ketki Jagtap, Karandeep Singh, Navneet Singh|
|Executing the query, and finding the correct results |Ketki Jagtap, Diksha Kumawat|
|Take screenshots and create the document|Navneet Singh, Karandeep Singh, Ketki Jagtap, Diksha Kumawat|

