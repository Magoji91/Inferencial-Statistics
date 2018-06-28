# Inferencial-Statistics

# 1 You hear about two studies looking at the effect of pollution on the number of birds in The Netherlands. Study1 counted birds in 20 parks, and study 2 counted birds in 100 parks. Which study is more likely to draw a conclusion that is representative of the population?

Study 2

#2 A busy traffic intersection in a city was experiencing an average of 20 accidents per week. The council decided to try to reduce the number of accidents by placing a stop sign at the intersection. In this situation, what is i) the null hypothesis, and ii) the alternative hypothesis?

μ1 −μ2=0;  μ_1 > μ_2

#3 Normally, about 40 people out of every 100 turn up for a local election. You show pictures of politicians with baby animals to a sample of 100 people, and measure their voting turnout. The null hypothesis is that pictures of baby animals do not influence voting turnout. You find a test statistic of 2.179, which corresponds to a two-sided p-value of less than 0.025. What can we say about this?

If the null hypothesis is true, the chance of finding that people’s voting habits are influenced by pictures of baby animals is less than 2.5%

#4 In an experiment on the effects of giving children candy on children’s test scores, you’re not sure which direction the effect will work. The candy may act as a reward that has a positive effect on scores, or it could make the children hyperactive so that they don’t concentrate very well on the tests.

The mean test score without candy was 25. The mean test score with candy was 20. We found that the 95% confidence interval for the group that ate candy ranged from 18.5 - 21.5. Which of the following is the case?

FALSE <- We can accept the null hypothesis, because there is a 95% chance that this would happen if the null hypothesis was true.
FALSE<- We can accept the null hypothesis because there is a 5% chance that this would happen if the null hypothesis was true.

We can reject the null hypothesis because there is a 5% chance that this would happen if the null hypothesis was true.

#5 If you reject the null hypothesis when the null hypothesis is true, what is this an example of?

Type I error

#6 Which of the following will improve statistical power? (select all that apply)

Increase the level of alpha
Reduce the variance in the population
Use more reliable measurement instruments

#7 A surprising number of people are scared of clowns. You expect that people will have more nightmares the night that they see clowns at the circus. To test this, you send a group of people to a circus with clowns, and a group to a circus without clowns, and measure the number of people in each group who have nightmares that night. Your data is shown below:

it<-matrix(c(12, 30, 35, 8), ncol=2)
colnames(it)<-c('Nightmares', 'Nice Dreams')
rownames(it)<-c('No clowns', 'Clowns')
it
result.prop<-prop.test(it)
result.prop

sqrt(21.894)
[1] 4.679102

#8 A lot of people were scared of clowns after seeing the horror movie IT about a killer clown. However, perhaps seeing a regular clown at the circus reduces this fear.

We examine two groups of people who have seen the movie ‘IT’, one group has been to the circus since seeing the film and one group has not. In the group that has been to the circus, the proportion of clown phobia is 0.016. In the group that has not been to the circus, the proportion of clown phobia is 0.034.

Calculate the relative risk of clown phobia if you don’t go to the circus after seeing the film ‘IT’.

x<-0.0160/0.034

#9 You expect that economics students like statistics more than art students, and decide to investigate.

You take a sample of 23 art students and 30 economics students, and measure how much they like statistics on a continuous scale. The mean amount that a group of economics students likes statistics is 26, while the mean amount that a group of art students likes statistics is 15. The variance in the economic group is 4.2, while the variance in the art group is 10.3.

Based on the size of the variances, would you assume the population variances are equal?

YES

#Question 10
In your sample of 23 art students and 30 economics students, the mean amount that a group of economics students like statistics is 26, while the mean amount that a group of art students like statistics is 15. The variance in the economic group is 4.2, while the variance in the art group is 10.3.

Calculate your test statistic for finding whether the groups differ in how much they like statistics.

n1=23
x1=15
sd1=10.3
n2=30
x2=26
sd2=4.2


x1 <- 15
x2 <- 26
s1 <- 10.3
s2 <- 4.2
n1 <- 23
n2 <- 26
diff_in_means <- x1 - x2
SE_diff_mean <- sqrt(s1^2/n1+s2^2/n2)
t_stat <- diff_in_means/SE_diff_mean
t_stat
-4.782125

pvalue = 2* pt(t_stat, df=n1+n2-2)
pvalue
 1.750188e-05
 
 #11 The average IQ in the population is 100, however there has been some research into how music changes this. You compared two samples of 300 people listening to either Michael Jackson or Mozart for an hour. You expected that mean IQ score in the Mozart group would be higher than the Michael Jackson group. The mean IQ score in the Mozart group was 130, while for the Michael Jackson group the mean was 90. The standard error across both groups was 4.47.

Calculate the upper boundary of the 95% confidence interval for the sample statistic. The critical t-value for this is 1.96.

#12 The average IQ in the population is 100, however there has been some research into how music changes this. You compared two samples of 300 people listening to either Michael Jackson or Mozart for an hour. You expected that mean IQ score in the Mozart group would be higher than the Michael Jackson group. The mean IQ score in the Mozart group was 130, while for the Michael Jackson group the mean was 90. The standard error across both groups was 4.47.

Calculate the lower boundary of the 95% confidence interval for the sample statistic. The critical t-value for this is 1.96.

n=300
X1=130
X2=90
n2=300
s1=4.47
s2=4.47


m1 <- c(130)
m2 <- c(90)
sd1 <- c(4.47)
sd2 <- c(4.47)
num1 <- c(300)
num2 <- c(300)
se <- sqrt(sd1*sd1/num1+sd2*sd2/num2)
error <- qt(0.975,df=pmin(num1,num2)-1)*se
left <- (m1-m2)-error
left
right <- (m1-m2)+error
right

#13 if we want to look at the effect of Mozart and Michael Jackson on IQ score and we have 100 willing participants on whom to test this, we have two options. Option 1 is to compare 50 participants that listen to Michael Jackson, and 50 participants that listen to Mozart. Option 2 is to measure IQ in all participants after listening to Mozart, and then measure IQ in all participants after listening to Michael Jackson.

Which of the following statements is/are correct? Select all that apply

For option 1 we would use an independent groups analysis.
For option 2 we would use a “dependent” or “matched” groups analysis.

#14 You’re interested in whether a life coach changes people’s feelings about exercising. You expect that people will like the gym more after meeting a life coach. You first look at whether or not people like the gym before meeting a life coach, then look at whether or not they like the gym after meeting a life coach. The table below shows the results.

1.517929376


#15 You are interested in the effects of alcohol on memory and run an experiment where people perform a memory test before and after consuming 6 beers. The table below shows the number of items remembered before beer (left column) and after beer (right column). The standard deviation of the difference score is 2.3.

xd = 0.4, t = 0.3888, fail to reject null hypothesis in two-sided test.

#16 If the relationship between X and Y occurs because X influences Z, which in turn influences Y, then Z is called a .... . If the the relationship between X and Y becomes weaker/stronger at different levels of Z, then Z is called a … . If controlling for Z completely removes the effect of X on Y, then Z is called a … .
Mediator, moderator, confounder.

#17 In a one-tailed test, your t-value is 2.61 with 18 df. With an alpha level of 0.05, which of the following is correct?
You would reject the null hypothesis.

#18 In a two-tailed test, your t-value is 1.85 with 19 df. With an alpha level of 0.05, which of the following is correct?
You would fail to reject the null hypothesis


