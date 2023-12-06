## Replicate scatter chart with two variables

#import data

head(iris)

#Create scatter plot

ggplot(data, aes(x = x, y = y)) +
  geom_point() +
  labs(title = "Two-Variable Scatter Plot",
       x = "X-axis",
       y = "Y-axis")
  ![image](https://github.com/yichao2022/yichao202310.github.io/assets/113857588/e2bfc129-acad-49b1-8a43-7ca66bba2030)

## bubble chart
#import dataset

data(iris)

  #Create bubble chart with ggplot2 and plotly

p <- ggplot(data, aes(x = x, y = y, z = z, size = size)) +
  geom_point(aes(color = size), alpha = 0.7, shape = 16) +
  scale_size_continuous(range = c(5, 15)) +
  scale_color_viridis_c() +
  theme_minimal()

#Convert ggplot to plotly

p <- ggplotly(p)
![image](https://github.com/yichao2022/yichao202310.github.io/assets/113857588/ce0fe2e9-6cd6-4acc-a98a-065d45c43166)


