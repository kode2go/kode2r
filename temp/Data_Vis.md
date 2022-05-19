```r
df <- midwest
df_s <- subset(df, select = c("county","state"))
View(df_s)
df_s <- subset(df, area 0.01,select = c("county","state","area"))
View(df_s)
df_s <- subset(df, area 0.1,select = c("county","state","area"))
View(df_s)
df_s <- subset(df, area 0.01 & popdensity 20000,select = c("county","state","area","popdensity"))
View(df_s)

df_s <- subset(df, area 0.01 & popdensity 20000,select = c("county","state","area","popdensity","percollege","percprof"))
View(df_s)
typeof(df_s)
class(df_s)
df_s_t <- as_tibble(df_s)

colnames(df_s_t)
[1] "county"     "state"      "area"       "popdensity" "percollege" "percprof"  
names(df_s_t)[names(df_s_t) == "percollege"] <- "college"
View(df_s_t)
names(df_s_t)[names(df_s_t) == "percprof"] <- "professional"
colnames(df_s_t)
[1] "county"       "state"        "area"         "popdensity"   "college"      "professional"
```

Question 2:

```r
df_s2 <- subset(df, category == "LAR" | category == "LHR",select = c("state","poptotal","popdensity","percollege","category"))
```

Question 3:

https://www.geeksforgeeks.org/melting-and-casting-in-r-programming/

Question 4:

```r
barplot(table(chickwts$weight,chickwts$feed))
```

![image](https://user-images.githubusercontent.com/29664888/169015982-2d39c622-745e-49a6-a7d8-8014e9048404.png)

```r
boxplot(chickwts$weight ~ chickwts$feed)
```

![image](https://user-images.githubusercontent.com/29664888/169015932-fdb521e5-e556-4f36-9af5-410d88c083ae.png)

```r
plot(chickwts$weight,col=chickwts$feed,main="Chick weights")
legend("topleft", levels(chickwts$feed), fill = c("blue","green","black","orange","red"))
```

![image](https://user-images.githubusercontent.com/29664888/169015792-5d2883cb-0c96-46de-bdec-64984c8c6d34.png)

```r
View(Orange)
df <- Orange
SP <- df$Tree
pie(table(SP))
boxplot(df)
counts <- table(Orange$Tree)
df <- as.factor(Orange$Tree)
age <- Orange$age
circum <- Orange$circumference
plot(age,circum)
plot(age,circum, col=df)
legend("topleft", level(df), fill = 1:3)
legend("topleft", levels(df), fill = 1:5)
plot(age,circum, col=df, main="Orange Data set")
legend("topleft", levels(df), fill = c("blue","green","black","red","orange"))
```

![image](https://user-images.githubusercontent.com/29664888/169016026-1fc53f2e-0dc7-461d-9b47-ab100f2ab7a0.png)

