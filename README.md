# MapReduce-Spark'
#####################
#java8
#eclipse
#spark
#hadoop


Implement the following exercises using MapReduce and Spark. 

Consider the movielens dataset provided with the partial code (see folder “movielens”). 
See: https://grouplens.org/datasets/movielens for a description of the dataset. 

1. (1 pt) Find the average rating for each user and movie. 
	Use MapReduce in Hadoop.
	Use the “ratings.csv” file. This file is copied to “input_movielens” subdirectory.
	Use the same MR program to compute both in one go. 
	Use a combiner (additionally to mapper and reducer).

2. (3 pt) Find the average rating for each genre.
	Use MapReduce in Hadoop.  
	Use the “movies.csv” file to find the genre of each movie.
	This file is assumed to fit in the memory of a machine; it is cached locally. 
	A movie can belong to multiple genres. 
  A rating of a movie should be used for all the genres the movie belongs in. 
	Use a combiner (additionally to mapper and reducer).

3. (1 pt) Repeat 1 using Spark.

4. (5 pt) Repeat 2 using Spark.

The partial code and Hadoop and Spark can be downloaded from: http://webhome.cs.uvic.ca/~thomo/assign3_hadoop_spark.zip 
(see the README file)







////////////////////////////////////////////////////////////////////////////////
***To Be Done First***
Set an enviroment variable:
HADOOP_HOME to point to the full path of hadoop-2.7.1
(This is system dependent. Find the way to do that in your system.)

Also, make sure you are using Java 8. 


Now open a terminal (Mac/Linux) or cmd (Windows). 
To try the examples in "hadoop_examples_post" do: 

cd hadoop_examples_post
javac -cp "../spark-2.1.0-bin-hadoop2.7/jars/*" -d bin src/*.java
 (Older version of Windows: change / to \)

One example is: 
  Mac/Linux
java -cp "../spark-2.1.0-bin-hadoop2.7/jars/*":bin MaxTemperature
  Windows:
java -cp "../spark-2.1.0-bin-hadoop2.7/jars/*";bin MaxTemperature

MaxTemperature: 
  reads data from folder "input_weather" and 
  outputs results in "output_weather". 
To see the results, do:
  Mac/Linux:
more output_weather/part-r-00000
  Windows:
more output_weather\part-r-00000

Leave the "hadoop_examples_post" directory by doing: 
cd ..



To try the examples in "SparkJava8Examples_post" do:

cd SparkJava8Examples_post
javac -cp "../spark-2.1.0-bin-hadoop2.7/jars/*" -d bin src/*.java
 (Older version of Windows: change / to \)

One example is: 
 Mac/Linux:
java -cp "../spark-2.1.0-bin-hadoop2.7/jars/*":bin SimpleAppSpark
 Windows:
java -cp "../spark-2.1.0-bin-hadoop2.7/jars/*";bin SimpleAppSpark

 
Remarks. 
1. Use Java 8.  

2. If you want to import the sources in Eclipse, use the latest version, Eclipse Neon. 
   Then add to the build path all the jars in folder spark-2.1.0-bin-hadoop2.7/jars

3. The partial code for Assignment 3 is in:
     hadoop_examples_post:    Movielens* files 
     SparkJava8Examples_post: SparkMovielens* files. 








