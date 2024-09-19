# Programming-Assignment-4

For the task we were first needed to create a dataframe from the an existing .xlsx file 

## We were tasked to 
Create the following data frames based on the format provided:

a. Filename: Instru = [“Name”, “GEAS”, “Electronics >70”]; where track is constant as Instrumentation and hometown Luzon

b. Filename: Mindy = [ “Name”, “Track”, “Electronics”, “Average >=55”]; where hometown is constant as Mindanao and gender Female

Create a visualization that shows how the different features contributes to average grade. Does chosen track in college, gender, or hometown contributes to a higher average score?

# Creating Filename: Instru = [“Name”, “GEAS”, “Electronics >70”]; where track is constant as Instrumentation and hometown Luzon

First in order to extract the data from the excel file I used 

###  pd.read_csv()

## then using the code grade.loc[(grade['Track'] == 'Instrumentation') & (grade['Hometown'] == 'Luzon') & (grade['Electronics'] > 70), ('Name','Electronics','GEAS')]

I was able to extract the specific parts that I needed from the table. 

## also through the use of .reset_index() 

I was able to reset the index of the new data frame that was created. 

# Creating Filename: Mindy = [ “Name”, “Track”, “Electronics”, “Average >=55”]; where hometown is constant as Mindanao and gender Female

For this part of the task it is the same as the last code, except with the addition of the code:

## grade['Average'] = grade[['Math','Electronics','GEAS','Communication']].mean(axis=1)

With this a new column was created and I am able to use it to get the next dataframe that is being asked. 

## with the final code being: Mindy = grade.loc[(grade['Hometown'] == 'Mindanao') & (grade['Gender'] == 'Female') & (grade['Average'] >= 55),['Name', 'Track', 'Electronics', 'Average']]

# Create a visualization that shows how the different features contributes to average grade. Does chosen track in college, gender, or hometown contributes to a higher average score?

For this task I needed to gather all the mean for the different features. And used a bar graph to illustrate the differences. 

### Based on the graphs, when it came to the track, the differences between Communication, Microelectronics and Instrumentation are very close with Communication being a little higher than the others

### Next when it came to gender, both Male and Female seemed to have the same average. And for the Hometown, Luzon has the little edge but they are almost all equal.

## Therefore the collage, gender, or hometown does not attribute to a higher or lower score according to the data gathered.

## What I learned

In this task we were able to utilize the use of pandas in addition to the used of matplotlib in order to visualize the data that was gathered. I also learned that it is important to keep your code readable and presentable as it would also make the debugging a lot easier. 
