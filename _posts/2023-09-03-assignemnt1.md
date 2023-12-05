---
title:  "Assignment 1"
mathjax: true
layout: post
categories: media
---
# Simple version
plot(anscombe$x1,anscombe$y1)
summary(anscombe)
![image](https://github.com/yichao2022/yichao202310.github.io/assets/113857588/a4cc4560-1ed1-498c-bb92-228645bb03b7)
# Create four model objects
lm1 <- lm(y1 ~ x1, data=anscombe)
summary(lm1)
lm2 <- lm(y2 ~ x2, data=anscombe)
summary(lm2)
lm3 <- lm(y3 ~ x3, data=anscombe)
summary(lm3)
lm4 <- lm(y4 ~ x4, data=anscombe)
summary(lm4)
plot(anscombe$x1,anscombe$y1)
abline(coefficients(lm1))
plot(anscombe$x2,anscombe$y2)
abline(coefficients(lm2))
plot(anscombe$x3,anscombe$y3)
abline(coefficients(lm3))
plot(anscombe$x4,anscombe$y4)
abline(coefficients(lm4))
![image](https://github.com/yichao2022/yichao202310.github.io/assets/113857588/b0d9616e-f0bf-48db-ae09-4991b4c9f05d)
#Fall.R

