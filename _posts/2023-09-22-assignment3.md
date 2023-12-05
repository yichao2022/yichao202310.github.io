
#Plot charts using for loop
the color of the outline of the plot character changed to yellow
the background color of the plot character changed to blue
the line representing the "line of best fit" from blue to green
for(i in 1:4) {
  ff[2:3] <- lapply(paste0(c("y","x"), i), as.name)
  plot(ff, data = anscombe, col = "yellow", pch = 23, bg = "blue", cex = 1.2,
       xlim = c(3, 19), ylim = c(3, 13))
  abline(mods[[i]], col = "green", lty = 4)
}
mtext("Anscombe's 4 Regression data sets", outer = TRUE, cex = 1.5)
par(op)
![image](https://github.com/yichao2022/yichao202310.github.io/assets/113857588/bed0d4ba-a05b-49c6-84be-fdd83f7537c7)

##plot the graph for scatterplot matrix;
 Download COVID data from OWID GitHub
owidall <- read.csv("https://github.com/owid/covid-19-data/blob/master/public/data/owid-covid-data.csv?raw=true")
 Deselect cases/rows with OWID
owidall <- owidall[!grepl("^OWID", owidall$iso_code), ]
Subset by continent: Europe
owideu <- subset(owidall, continent=="Europe")

date <- as.Date(owideu$date, format = "%Y-%m-%d")
deaths <- owideu$new_deaths

plot(date, deaths, type = "p", ylim = c(0, 7000), xlab = "Date",
     ylab = "COVID Deaths in Europe (Daily)", col = "magenta2", pch = 16, 
     cex = 0.7)
par(las = 2)
axis.Date(1, at = seq(min(date), max(date), by = "2 months"), 
          format = "%m-%Y")
axis(2, at = seq(0, max(y), by = 1000))
par(mar = c(5, 4, 1, 1) + 0.1, cex.axis = 0.6)
text(x = as.Date("2020-04-15"), y = 6000, labels = "Spain", cex = 0.5)
text(x = as.Date("2020-04-18"), y = 5000, labels = "Spain", cex = 0.5)
text(x = as.Date("2020-12-01"), y = 6500, labels = "Germany", cex = 0.5,
     pos = 3)
text(x = as.Date("2021-11-01"), y = 5000, labels = "Ukraine", cex = 0.5)
text(x = as.Date("2023-01-01"), y = 1500, labels = "Germany", cex = 0.5)
text(x = as.Date("2023-09-20"), y = 500, labels = "Italy", cex = 0.5)## Download COVID data from OWID GitHub
owidall <- read.csv("https://github.com/owid/covid-19-data/blob/master/public/data/owid-covid-data.csv?raw=true")
 Deselect cases/rows with OWID
owidall <- owidall[!grepl("^OWID", owidall$iso_code), ]
 Subset by continent: Europe
owideu <- subset(owidall, continent=="Europe")

date <- as.Date(owideu$date, format = "%Y-%m-%d")
deaths <- owideu$new_deaths

plot(date, deaths, type = "p", ylim = c(0, 7000), xlab = "Date",
     ylab = "COVID Deaths in Europe (Daily)", col = "magenta2", pch = 16, 
     cex = 0.7)
par(las = 2)
axis.Date(1, at = seq(min(date), max(date), by = "2 months"), 
          format = "%m-%Y")
axis(2, at = seq(0, max(y), by = 1000))
par(mar = c(5, 4, 1, 1) + 0.1, cex.axis = 0.6)
text(x = as.Date("2020-04-15"), y = 6000, labels = "Spain", cex = 0.5)
text(x = as.Date("2020-04-18"), y = 5000, labels = "Spain", cex = 0.5)
text(x = as.Date("2020-12-01"), y = 6500, labels = "Germany", cex = 0.5,
     pos = 3)
text(x = as.Date("2021-11-01"), y = 5000, labels = "Ukraine", cex = 0.5)
text(x = as.Date("2023-01-01"), y = 1500, labels = "Germany", cex = 0.5)
text(x = as.Date("2023-09-20"), y = 500, labels = "Italy", cex = 0.5)

![image](https://github.com/yichao2022/yichao202310.github.io/assets/113857588/c8019dd1-6613-4b57-aec7-2b55d78e3774)

