# EmergingTechTaskProject


## Intro
This Project is for 4th Year Software Development Semester 1's module "Emerging Technology".<br/>
The goal of this project is to use the Jupyter Notebook to do various tasks of different topics. It is to increase our own ability to self learn and expand our knowledge in both Python and other functioning libraries.<br/>
It is wrote in the Python programming language Version 3.<br/>
The Jupyter Notebook is an open-source web application that allows you to create and share documents that contain live code, equations, visualizations and narrative text. Uses include: data cleaning and transformation, numerical simulation, statistical modeling, data visualization and machine learning.<br/>
<img height="300" width="600" src="https://miro.medium.com/max/3840/1*R5uM8zw8uhW4-HC4F1v9IA.png" />

## Installation
### Step 1
git clone https://github.com/CathalDonohoe/EmergingTechTaskProject <br/>
<img height="100" src="https://gyazo.com/2de6a6c0d18982743012ef8ddf0b5e5c.png"/>
### Step 2
Then direct to the folder that you have cloned the repository to. from there click on the path and type cmd.
<img src="https://gyazo.com/c9cf06233d5c938b08e68888a9c47eda.png"/>
### Step 3
From here type "jupyter notebook" and run it. </br>
<img src="https://gyazo.com/a307423d2ae7333ec5da3ff07b0515f3.png"/>
### Step 4
This will open a tab on your browser.
Proceed to click on the .ipynbd
<img src="https://gyazo.com/d13731cfeb220fb235855678ead6eb78.png"/>
After this you may need to edit task 4. Task 4 takes in the Iris data set from a file directory. As it is expected, your file locqation for the Iris dataset will be different. Please edit this line of code here in order for it to work: </br>
<img src="https://gyazo.com/a04437d05cb4c72a5aae33cafcd840b9.png"/> </br>
After this, hit the Kernal tab and click "Restart & Run All". </br>

## Tasks
</br>

### Task 1

This Task involves finding the square route of the number 2, and printing it to 100 decimal places. According to Collins dictionary the definition of the square root is "The square root of a number is another number which produces the first number when it is multiplied by itself. For example, the square root of 16 is 4." So the objective of this task is to get the number that when multiplied by itself is equal to 2. The code however cannot depend on any module from the standard library or otherwise. One of the methods we can use to do this is Newtons method. We could us this to print out the square root of 2 very simply. However, as this is coded in python, its print method will only print a float value up to 52 places after the decimal point.
To work against this we use a googol. A googol is essentially 10 to the power of 100. multiplying 2 by googol to the power of 2 will give use the square root and move it to 100 decimal places from the decimal point. After this I floor devision to bit shift the number to the left of the decimal place. Floor division is a normal division operation except that it returns the largest possible integer. This integer is either less than or equal to the normal division result.I then convert this number to a string.m I use the ".find()" function to find the first instance of the number 4 in the string, as we know the first number after 1 in the square root of 2 is 4. Then I insert a decimal place before this number and print out the string giving us this:
<img src="https://gyazo.com/c0e466f964884a2be4804ca4b4dab770.png"/>
</br>

### Task 2

Task 2 involves using the Chi-Square test to varify the chi-squared value. We do this by using pre-defined data given to us.</br>
<img src = "https://gyazo.com/7eebeadd511a9a2ab15af386e4acaca2.png" /> </br>
The Chi-squared test is a statistical hypothesis test determines whether there is an association between catagorical variables. This basically means it can find out if variables are independant or related to one another. Chi-square tests are often used in hypothesis testing. The chi-square statistic compares the size of any discrepancies between the expected results and the actual results, given the size of the sample and the number of variables in the relationship.</br>
Chi-square formula below:</br>
<img src="https://gyazo.com/e5528137c77226c1056fee0eb7f54cc6.png"/> </br>
I first created a dataset with the with the data given to us in the brief. I did this by creating an array with multiple sets like so: </br>
<img src="https://gyazo.com/6c0c407e16edf0ce2eb25f9814bc77ac.png"/></br>
After this i use the stats.chi_contingencey function to execute the chi square test on the data. When we do this we can get the Chi value, the p value and the expected values by doing so: </br>
<img src="https://gyazo.com/c8fd667bf3f84912597aff53786745e6.png"/> </br>
After doing this, we simply need to print the values to confirm the Chi-squared value and to get the P-value: </br>
<img src="https://gyazo.com/598e7aeee0d39b91daa9b6960a3628de.png"/> </br>
This confirms that the associated Chi-squared value is indeed 24.6 and that the P-value is 0.00409.
</br>

### Task 3

Task 3 goal is to compare Standard deviation funcitons.  Microsoft  Excel  has  two  different  versions  of  the  standard  deviationc alculation, STDEV.P and STDEV.S. The main difference between these two functions is the formula. Where STDEV.P's funciton is: </br>
### np.sqrt(np.sum((x - np.mean(x))**2)/len(x)) </br>
STDEV.S's fucntion is: </br>
### np.sqrt(np.sum((x - np.mean(x))**2)/len(x)-1). </br>
Now there is very little difference in the formulas but the output will be different. We are tasked with demonstrating that the STDEV.S function is a better estimate than the STDEV.P funciton.</br>
To do this I first calculated the standard deviation on a whole population: </br>
<img src="https://gyazo.com/b0bae931f6873598131560eb3f9c68c4.png"/></br>
This tells us that the Standard Deviation for that Data is 27.706. From here we simply need to execute the other two funstions, with the same sample population, and see their outputs: </br>
<img src="https://gyazo.com/ddfeb40c2a12306f77800663d8d764ec.png"/></br>
From here we can see that STDEV.P return 33.508, whereas STDEV.S returns to us 33.493. As STDEV.S's return is closer to the actual standard deviation, we can deduce that STDEV.S is a more accurate estimate of the standard deviation than STDEV.P. </br>

### Task 4

Task 4 objective is to use the Sckit-learn to apply k-means clustering to Fishers Iris Data set. The Iris flower data set or Fisher's Iris data set is a multivariate data set introduced by the British statistician, eugenicist, and biologist Ronald Fisher in his 1936 paper The use of multiple measurements in taxonomic problems as an example of linear discriminant analysis. The data set consists of 50 samples from each of three species of Iris (Iris setosa, Iris virginica and Iris versicolor). Four features were measured from each sample: the length and the width of the sepals and petals, in centimeters. Based on the combination of these four features, Fisher developed a linear discriminant model to distinguish the species from each other. </br>
We can use k-means clustering to demonstrate this data visually. k-means clustering is a method of vector quantization that aims to partition n observations into k clusters in which each observation belongs to the cluster with the nearest mean, serving as a prototype of the cluster. </br>
To do this we import the kmeans from sklearn.cluster. We then read in the Iris dataset. There are multiple ways of doing this, but I opted to import it from a file location. After this we put the data from the csv file into arrays. I then stack the 4 arrays(from the 4 columns in the csv) into 2 variables. I then concatenate them into a master dataset. </br>
I fit the dataset with 3 clusters. Then i assign each cluster a colour and shape to differentiate them from eachother. Then after setting up centers for the clustersi plot it onto the screen with this output: </br>
<img src="https://gyazo.com/d3ca883809d046797f7c0109bfe2fb1e.png"/> </br>
The brief specifies that we should demonstrate predictions within our code. So i made du8mmy data and place it into a data set. I give these a different shape and colour and print them out with the plot:
</br>
<img src="https://gyazo.com/9da42eaa762121e2ff6bda600d84d08e.png"/> </br>


## Research for Project
### Task 1
[1] [ps://www.educative.io/edpresso/floor-division] (Even shows floor division in python)  <br/>
[2] [https://stackoverflow.com/questions/4022827/insert-some-string-into-given-string-at-given-index-in-python]  <br/>
[3] [tour of Go: https://tour.golang.org/flowcontrol/8]  <br/>
[4] [http://mathforum.org/library/drmath/view/65402.html]  <br/>
[5] [http://resources.esri.com/help/9.3/arcgisengine/java/gp_toolref/spatial_analyst_tools/how_bitwise_left_shift_works.htm#:~:text=For%20each%20bit%20in%20the,farthest%20left%20bit%20is%20lost]  <br/>
[6] [https://en.wikipedia.org/wiki/Googol]  <br/>

### Task 2
[1][https://www.w3schools.com/python/python_lists.asp] <br/>
[2][https://www.pythoncentral.io/the-difference-between-a-list-and-an-array/#:~:text=The%20main%20difference%20between%20a,you%20can%20perform%20to%20them.&text=It%20does%20take%20an%20extra,fine%20most%20of%20the%20time] <br/>
[3][https://stackoverflow.com/questions/39497519/easiest-way-to-make-data-frames-in-python-without-pandas-package] <br/>
[4][https://pythonhealthcare.org/2018/04/13/58-statistics-chi-squared-test/] <br/>
[5][http://hplgit.github.io/primer.html/doc/pub/looplist/._looplist-bootstrap004.html] <br/>
[6][https://www.investopedia.com/terms/c/chi-square-statistic.asp] <br/>
[7] [https://docs.scipy.org/doc/scipy/reference/generated/scipy.stats.chi2_contingency.html] <br/>

### Task 3
[1][https://exceljet.net/excel-functions/excel-stdev.p-function] <br/>
[2][https://exceljet.net/excel-functions/excel-stdev.s-function] <br/>
[3][https://www.tutorialspoint.com/python/python_strings.htm] <br/>
[4][https://en.wikipedia.org/wiki/Standard_deviation] <br/>
[5][https://www.exceltip.com/statistical-formulas/how-to-use-excel-stdev-p-function.html] <br/>
[6][https://www.mrexcel.com/board/threads/stdev-p-vs-stdev-s.973223/] <br/>

### Task 4
[1][https://scikit-learn.org/stable/auto_examples/datasets/plot_iris_dataset.html] <br/>
[2][https://matplotlib.org/3.1.1/api/markers_api.html] <br/>
[3][https://en.wikipedia.org/wiki/Iris_flower_data_set] <br/>
[4][https://datahub.io/machine-learning/iris] <br/>
