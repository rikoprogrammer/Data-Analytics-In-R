# Data Analytics In R
## Introduction
## Data types
## Reading data
## Data manipulation
## Sample project on analytics
# Introduction
R is a programming language with easy syntax to learn. Its dynamically typed so you don't have to specify a data type of a variable before using it.<br>
R is widely used in data science, machine learning and general data analytics tasks.<br> In this short course you will learn how to leverage the power of R to analyse any data set at your disposal.<br>
To install R please visit this site(windows users) https://cran.r-project.org/bin/windows/base/ <br>
For Mac and other systems please just google how to install R on mac/linux etc and you will be guided on how to install R on your system.<br>
Once you have R on your system, you can run commands either using an editor or directly from R command line interface.<br>
When you open R this is what you see: <br>
![R console](console.png)
<br>
You can start typing commands directly in this console. To print Hello R on the screen simply type <i>print("Hello R")</i> You can use either single quotes or double quotes.<br>
The print <i>keyward</i> is optional, you can simply type <i>'Hello R'</i>
# Data types
## Primitive data types
1. <b>Integer</b> <br>
Represents the numerics, can either be whole numbers a.k.a integers or decimals a.k.a doubles.

2. <b>Character/string</b><br>
Represents text data, use either single quotes or double quotes to denote text.

3. <b>Boolean</b><br>
Represents either true or false data types. Represented in R with TRUE/FALSE or T/F

4. <b>Complex</b><br>
These are rarely used, they denote complex numbers. They take this form <i>a + bi</i> where a and b are real numbers.

5. <b>Raw</b><br>
These are also rarely used. They represent raw bytes of information.

## Collection data types
1. <b>Vectors</b> <br>
vectors denote a collection that contains objects of a single data type. A vector is one dimensional.<br>
We create a vector in R with <i>c()</i> command which means concatenate. Example: <i>my_vec = c(2,4,6.7,77)</i>

2. <b>Matrices</b> <br>
These are two dimensional data structures, they have rows and columns. They can only contain a single data type.<br>
You define a matrix with the matrix function e.g <i>my_mat = matrix(1:6,2,3)</i>. First argument gives a set of matrix elements then the second and third arguments specify dimensions.

3. <b>Lists</b> <br>
This collection is heterogeneous in the sense that it can accept objects of multiple data types. You define a list with the <i>list()</i> command as follows; <i>my_list = list(23,'books',my_vector)</i>

4. <b>Arrays</b> <br>
These are multidimensional data structures. A matrix is a special type of an array with only two dimensions.<br>
You define an array with the <i>array()</i> function as follows; my_array = array(1:10,dim = c(2,3,4))

5. <b>Data Frames</b> <br>
This is the most common data structure used in data analytics. It's analogous to a spreadsheet but with a nicer interface. It can accept objects with multiple data type but with a restriction that each column is supposed to be a single data type.<br>
You can think of it as a collection of vectors of equal length.<br>
To create a data frame you need to first have your vectors, example:<br>
names = c('Mato','Fely')<br>
age = c(22,34)<br>
my_data_frame = data.frame(names,age)

6. <b>Factors</b> <br>
This data structure is used to store a categorical variable,i.e a variable that has a defined set of inputs eg gender has only male or female. If you have a character vector representing gender you can easily convert it into a factor by the <i>factor()</i> function

7. <b>Classes</b> <br>
You only define a class when you need to implement your own data type. A class serves as a blueprint from which you can create objects. R supports S3, S4 and R6 classes. This is an advanced topic please consult an advanced textbook on R

8. <b>Date time</b> <br>
This represents the date and time classes in R. R has support for as.POSIXlt(), as.POSIXct() and as.Date() functions that can help you deal with dates.

9. <b>Time series</b> <br>
This is used to represent time series data, commonly used in time series focusting and financial modeling.

# Reading Data
If you can't load your data into R then you can't work with it.<br>
In most data analytics work people deal with text files which provide a defacto standard for sharing data. To import a text file like a comma separated values(csv) file you use the <i>read.csv()</i> function. <br>This function accepts the name of the file being imported. N/B: Make sure that your file is in your working directory, if not you will have to specify the full path to your file.<br>
There are so many functions for importing data from other systems like SPSS or even data bases.

# Data Manipulation/Preprocessing
This involves checking if your data is useful enough for future analysis. <br>A sample workflow might be something like:<br>
>Check for missing data<br>
 Check for duplicates<br>
 Check the structure of your data like how many dimensions does it have<br>
 Whether you should feature scale your variables or not<br>
 Check the data type of each column to determine the kind of analysis is required.


# Sample Poject
## Objective
The objective of this project is to predict the salary of a new employee at a fictious company. <br>
We would like to know in advance what a posible position/job pays as the salary using a technique called support vector regression, you can as well use simple linear regression



