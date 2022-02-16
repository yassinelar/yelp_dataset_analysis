# yelp_dataset_analysis

The <b> Yelp dataset </b> is a subset of businesses, reviews, and user data of the US. Available as JSON files, it is used to learn about databases and NLP, or for sample production data.

Link to download the dataset (4,4 GB): https://www.yelp.com/dataset/download

In this notebook, we are going to use spark to manipulate data.

Before starting, it is essential to install and configure spark by executing the notebook's first cells.

<h3> To install spark: </h3>

```!apt-get install openjdk-8-jdk-headless -qq > /dev/null```

```!wget https://dlcdn.apache.org/spark/spark-3.0.3/spark-3.0.3-bin-hadoop2.7.tgz && tar xf spark-3.0.3-bin-hadoop2.7.tgz```

```!pip install pyspark==3.0.3 findspark```
  
<h3> To configure spark: </h3>

```import os```

```os.environ["JAVA_HOME"] = "/usr/lib/jvm/java-8-openjdk-amd64"```

```os.environ["SPARK_HOME"] = "/content/spark-3.0.3-bin-hadoop2.7"```

```import findspark```

```findspark.init()```

<h2> Abstract </h2>

In the first part of the project, the objectif is to manipulate data and display world's maps using the <b> folium library </b>.

For example, a map showing the number of establishment listed by Yelp in each country, the average stars or reviews per country...

![photo](https://user-images.githubusercontent.com/71329302/154366477-ae693fef-a86b-455e-b8aa-1d3a2c80ea58.jpg)

In the second part, the objectif is to define a classifier that predicts sentiment associated with a review ("positif" or "negatif"). 

The model generates then a score (list of 2 elements): the first element is the score of a positif review. The second one is the score of a negatif review.

![Capture](https://user-images.githubusercontent.com/71329302/154368594-db7c7bee-f501-45bc-8e28-16d58ae5a868.JPG)


