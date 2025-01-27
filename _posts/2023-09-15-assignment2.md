#Start plotting from basics 

plot(pressure, pch=11)  
text(150, 600, 
     "Pressure (mm Hg)\nversus\nTemperature (Celsius)")## Start plotting from basics 

plot(pressure, pch=16)  
text(150, 600, 
     "Pressure (mm Hg)\nversus\nTemperature (Celsius)")
![image](https://github.com/yichao2022/yichao202310.github.io/assets/113857588/e47b86dc-b90e-41a4-80b3-e16c07a6ef7d)

#Setting label orientation, margins c(bottom, left, top, right) & text size

par(las=1, mar=c(4, 4, 2, 4), cex=.8) 
plot.new()
plot.window(range(x), c(0, 6))
lines(x, y1)
lines(x, y2)
points(x, y1, pch=16, cex=2) # Try different cex value?  
points(x, y2, pch=21, bg="white", cex=2)  # Different background color
par(col="black", fg="gray50", col.axis="gray50")
axis(1, at=seq(0, 16, 4)) # What is the first number standing for?
axis(2, at=seq(0, 6, 2))
axis(4, at=seq(0, 6, 2))
box(bty="u")
mtext("Travel Time (s)", side=1, line=2, cex=0.8)
mtext("Responses per Travel", side=2, line=2, las=0, cex=0.8)
mtext("Responses per Second", side=4, line=2, las=0, cex=0.8)
text(4, 5, "Bird 131")
par(mar=c(5.1, 4.1, 4.1, 2.1), col="black", fg="black", col.axis="black")
![image](https://github.com/yichao2022/yichao202310.github.io/assets/113857588/c1058808-9c56-485f-8420-783c1ab0392d)

# Histogram

Y <- rnorm(50)
#Y no exceed [-3.5, 3.5]

Y[Y < -3.5 | Y > 3.5] <- NA # Selection/set range
x <- seq(-3.5, 3.5, .1)
dn <- dnorm(x)
par(mar=c(4.5, 4.1, 3.1, 0))
hist(Y, breaks=seq(-3.5, 3.5), ylim=c(0, 0.5), 
     col="gray80", freq=FALSE)
lines(x, dnorm(x), lwd=2)
par(mar=c(5.1, 4.1, 4.1, 2.1))

![image](https://github.com/yichao2022/yichao202310.github.io/assets/113857588/69ef5d3f-ff4d-47a7-a079-a86bc3c5d222)

# Barplot

par(mar=c(2, 3.1, 2, 2.1)) 
midpts <- barplot(VADeaths, 
                  col=gray(0.1 + seq(1, 9, 2)/11), 
                  names=rep("", 4))
mtext(sub(" ", "\n", colnames(VADeaths)),
      at=midpts, side=1, line=0.5, cex=0.5)
text(rep(midpts, each=5), apply(VADeaths, 2, cumsum) - VADeaths/2,
     VADeaths, 
     col=rep(c("red", "green"), times=3:2), 
     cex=0.8)
par(mar=c(5.1, 4.1, 4.1, 2.1))  
![image](https://github.com/yichao2022/yichao202310.github.io/assets/113857588/e96a637a-b9f9-4b44-9e94-108facb1baed)


# Boxplot

par(mar=c(3, 4.1, 2, 0))
boxplot(len ~ dose, data = ToothGrowth,
        boxwex = 0.25, at = 1:3 - 0.2,
        subset= supp == "VC", col="white",
        xlab="",
        ylab="tooth length", ylim=c(0,35))
mtext("Vitamin C dose (mg)", side=1, line=2.5, cex=0.8)
boxplot(len ~ dose, data = ToothGrowth, add = TRUE,
        boxwex = 0.25, at = 1:3 + 0.2,
        
        subset= supp == "OJ")
legend(1.5, 9, c("Ascorbic acid", "Orange juice"), 
       fill = c("red", "green"), 
       bty="n")
![image](https://github.com/yichao2022/yichao202310.github.io/assets/113857588/09c6cf4f-3d63-4b54-92e0-89ff3bc0734f)

# Persp

x <- seq(-10, 10, length= 30)
y <- x
f <- function(x,y) { r <- sqrt(x^2+y^2); 10 * sin(r)/r }
z <- outer(x, y, f)
z[is.na(z)] <- 1
#0.5 to include z axis label

par(mar=c(0, 0.5, 0, 0), lwd=0.5)
persp(x, y, z, theta = 30, phi = 30, 
      expand = 0.5)
par(mar=c(5.1, 4.1, 4.1, 2.1), lwd=1)

par(mar=c(5.1, 4.1, 4.1, 2.1))
![image](https://github.com/yichao2022/yichao202310.github.io/assets/113857588/efd42238-efcc-4f2a-889e-3a6c0d8beef1)

# Piechart
par(mar=c(0, 2, 1, 2), xpd=FALSE, cex=0.5)
pie.sales <- c(0.12, 0.3, 0.26, 0.16, 0.04, 0.12)
names(pie.sales) <- c("Blueberry", "Cherry",
                      "Apple", "Boston Cream", "Other", "Vanilla")
pie(pie.sales, col = gray(seq(0.3,1.0,length=6))) 

![image](https://github.com/yichao2022/yichao202310.github.io/assets/113857588/b3958d2a-3ac6-40c5-8f48-3c439b3d8337)

