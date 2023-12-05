df <- data.frame(Category = c("Item1", "Item1", "Item2", "Item2"),
Variable = c("Var1", "Var2", "Var1", "Var2"),
Value = c(15, 10, 12, 8))

library(ggplot2)

ggplot(df, aes(x = Category, y = Value, fill = Variable)) +
geom_bar(stat = "identity", position = "dodge") +
labs(title = "a column chart for Two Items",
x = "Items",
y = "Value") +
scale_fill_manual(values = c("Var1" = "black", "Var2" = "black")) +
theme_minimal()
![image](https://github.com/yichao2022/yichao202310.github.io/assets/113857588/27d23560-94be-43d9-a1b0-f255aa0b7cbd)

#Sample data frame

data <- data.frame(Item = c("Item1", "Item2", "Item3", "Item4","Item5","item6","item7","item8"),
Value1 = c(30, 45, 25, 60, 35,40,31,37),
Value2 = c(20, 40, 50, 30, 45,21,65,35))

#Load the ggplot2 library

library(ggplot2)

#Create the first horizontal bar chart

chart1 <- ggplot(data, aes(x = Value1, y = Item, fill = Item)) +
geom_bar(stat = "identity", orientation = "y") +
labs(title = "", x = "Value", y = "Item") +
theme_minimal() +
theme(axis.text.y = element_text(hjust = 1)) # Right-align item labels

#Create the second horizontal bar chart

chart2 <- ggplot(data, aes(x = Value2, y = Item, fill = Item)) +
geom_bar(stat = "identity", orientation = "y") +
labs(title = "", x = "Value", y = "Item") +
theme_minimal() +
theme(axis.text.y = element_text(hjust = 1)) # Right-align item labels

#Display the charts side by side

library(gridExtra)

grid.arrange(chart1, chart2, ncol = 2)

![image](https://github.com/yichao2022/yichao202310.github.io/assets/113857588/7f0ebbfa-01d0-48fc-85fa-0d9014104472)

chart 4

#Sample data frame

data <- data.frame(Item = c("Item1", "Item2", "Item3"),
Variable1 = c(10, 15, 20),
Variable2 = c(5, 8, 12))

#Load the ggplot2 library

library(ggplot2)

#Reshape the data from wide to long format using tidyr

library(tidyr)
data_long <- pivot_longer(data, cols = starts_with("Variable"),
names_to = "Variable",
values_to = "Value")

#Create the grouped bar chart

ggplot(data_long, aes(x = Item, y = Value, fill = Variable)) +
geom_bar(stat = "identity", position = position_dodge(width = 0.9)) +
labs(title = "Comparison of Variables for Three Items",
x = "Items",
y = "Value") +
theme_minimal()
![image](https://github.com/yichao2022/yichao202310.github.io/assets/113857588/dab4c09f-fcd1-4bd6-a82d-2c0997ba5999)

