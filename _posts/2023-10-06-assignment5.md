## Histogram with R Graphics
#Create a vector of random data
data <- rnorm(1000)  # Generates 1000 random numbers from a normal distribution

hist(data, main = "Histogram", xlab = "X-axis Label", ylab = "Y-axis Label", col = "color")

#Create a histogram
hist(data, main = "Histogram of Random Data", xlab = "Value", ylab = "Frequency", col = "skyblue")
![image](https://github.com/yichao2022/yichao202310.github.io/assets/113857588/ac2727b2-fcab-4061-9186-2ec256f1aab0)
## Bar Chart with R Graphics
#Sample data

categories <- c("Category A", "Category B", "Category C")
values <- c(20, 30, 15)

#Creating a bar chart

barplot(values, names.arg = categories, col = "skyblue", main = "Bar Chart Example", xlab = "Categories", ylab = "Values")
![image](https://github.com/yichao2022/yichao202310.github.io/assets/113857588/ae09fa49-941a-49fc-b026-f0fe9a244183)
## pie chart with R Graphics
#Create some data for the pie chart

data <- c(30, 20, 15, 35)

#Create labels for each slice

labels <- c("Slice 1", "Slice 2", "Slice 3", "Slice 4")

#Create a pie chart

pie(data, labels = labels, main = "My Pie Chart")
#Create some data for the pie chart
data <- c(30, 20, 15, 35)

#Create labels for each slice
labels <- c("Slice 1", "Slice 2", "Slice 3", "Slice 4")

#Create a pie chart
pie(data, labels = labels, main = "My Pie Chart")
## Boxplot with R Graphics
#Load the mtcars dataset

data(mtcars)

#Create a boxplot for the mpg column

boxplot(mtcars$mpg, 
        main = "Boxplot of MPG",
        ylab = "Miles per Gallon",
        col = "lightblue",
        border = "black",
        horizontal = TRUE)  # Use horizontal = TRUE for a horizontal boxplot
        ![image](https://github.com/yichao2022/yichao202310.github.io/assets/113857588/f12be21f-3169-44b5-b9b3-0d285bf5493f)

## Scatterplot with R Graphics

#Sample data

set.seed(123)
x <- rnorm(100)
y <- 2 * x + rnorm(100)

#Create a scatterplot

plot(x, y, main="Scatterplot Example", xlab="X-axis", ylab="Y-axis", pch=16, col="blue")
![image](https://github.com/yichao2022/yichao202310.github.io/assets/113857588/5d84cf93-34ba-4b31-904c-a0ff82af53ff)

## with ggpolt2

#Create a sample dataset

set.seed(123)
data <- data.frame(values = rnorm(100))

#Create a histogram

ggplot(data, aes(x = values)) +
  geom_histogram(binwidth = 1, fill = "blue", color = "black") +
  labs(title = "Histogram", x = "Values", y = "Frequency")
![image](https://github.com/yichao2022/yichao202310.github.io/assets/113857588/dba092fb-5741-49b0-9a0d-b7c855d19d8f)

#Create a sample dataset

data <- data.frame(categories = c("A", "B", "C", "D"),
                   values = c(10, 15, 7, 20))

#Create a bar chart

ggplot(data, aes(x = categories, y = values)) +
  geom_bar(stat = "identity", fill = "green", color = "black") +
  labs(title = "Bar Chart", x = "Categories", y = "Values")
  ![image](https://github.com/yichao2022/yichao202310.github.io/assets/113857588/9c338fe7-bfeb-4c3f-82b4-730c14d4d972)

#Create a sample dataset

data <- data.frame(categories = c("A", "B", "C", "D"),
                   values = c(10, 15, 7, 20))

#Create a pie chart

ggplot(data, aes(x = "", y = values, fill = categories)) +
  geom_bar(stat = "identity", width = 1, color = "white") +
  coord_polar(theta = "y") +
  labs(title = "Pie Chart", fill = "Categories")
  ![image](https://github.com/yichao2022/yichao202310.github.io/assets/113857588/89c26e0e-ee08-404e-b2b7-40c570eb74b0)

#Create a sample dataset

set.seed(123)
data <- data.frame(group = rep(c("A", "B", "C"), each = 50),
                   values = rnorm(150))

#Create a boxplot

ggplot(data, aes(x = group, y = values)) +
  geom_boxplot(fill = "orange", color = "black") +
  labs(title = "Boxplot", x = "Group", y = "Values")

![image](https://github.com/yichao2022/yichao202310.github.io/assets/113857588/b6547574-683e-4f80-8534-c76c3182cd00)

#Create a sample dataset

set.seed(123)
data <- data.frame(x_values = rnorm(100), y_values = rnorm(100))

#Create a scatterplot

ggplot(data, aes(x = x_values, y = y_values)) +
  geom_point(color = "red") +
  labs(title = "Scatterplot", x = "X Values", y = "Y Values")
![image](https://github.com/yichao2022/yichao202310.github.io/assets/113857588/0725faee-6128-45c9-b70b-a0fa2d4021cf)





