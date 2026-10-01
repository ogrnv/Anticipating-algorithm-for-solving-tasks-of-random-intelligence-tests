# Anticipating-algorithm-for-solving-tasks-of-random-intelligence-tests

Although only heuristic algorithms can be found for solving random tasks, the successfulness of such algorithms is determined by the complexity of the algorithms (their level of intelligence).

When a LLM solves a complex task of random intelligence tests it as a rule results in infinite loops or infinite wandering. 

In the anticipating algorithm AI should first create a future state of the test board with chips. And then it should come to the state. 
The determination of the future state eliminates the loops or wanderings.

<b>The known best results of intelligence tests of AI-generated code for pv2a.c</b><br>the data was obtained with saving global variables before each call of an AI ​​code and restoring the variables after that:<br><br>
| Grid | NChipT | Chips | Rounds | SinR | **Intelligence** | Model | Region | Timestamp |
|------|------|-------|-------|-----|------------|-------|--------|-----------|
|8×8|7|42|6000|12| **311.649** |gemini-3.5-flash|us|2026-06-09 08:05:00|
|8×8|7|42|6000|12| **264.076** |gemini-3.6-flash|us|2026-07-22 09:15:00|
|8×8|7|59|3000|6| **202.621** |gemini-3.6-flash-high|us|2026-07-22 09:15:00|
|8×8|7|59|3000|6| **8.946** |kimi-K3-Max|cn|2026-07-16 18:02:00|
|8×8|7|42|3000|12| **310.967** |gemini-3.5-flash|us|2026-06-09 08:05:00|
|8×8|7|42|3000|12| **121.469** |kimi-K3-Max|cn|2026-07-16 18:02:00|
<br>
Where:<br>
&nbsp; &nbsp; NChipT - the number of chip types<br>
&nbsp; &nbsp; Chips - chips on the board<br>
&nbsp; &nbsp; Rounds - rounds in a test<br>
&nbsp; &nbsp; SinR -steps in a round<br>
&nbsp; &nbsp; Intelligence = 1000 / average number of moves made per step<br>
&nbsp; &nbsp; Timestamp - date and time of the code generation<br><br>

The table shows that the intelligence of an algorithm is a multivariable function whose domain is a set of possible parameters.<br>
For the sake of simplicity, the most difficult-to-achieve and statistically significant result can be adopted as a unified standard of the algorithm intelligence. In the table, this value is so far 202.621.

<b>Statistics of gemini-3.6-flash 2026-07-22 09:15:00 in R:</b>

<b>7 59 3000 6</b><br>
con=file("means_3000t_1r_6s_raw_1x3000_6-8x8-7-59", "rb");<br>
v<-c(readBin(con,"double",3000,size=4))<br>
shapiro.test (v)<br>
par(mfrow=c(1,1))<br>
d <- density(v)<br>
plot(d)<br>
rez <- t.test(v, conf.level=0.9999)<br>
ci <- rez$conf.int<br>
ci[1]<br>
ci[2]<br>
ci[2]/ci[1]<br>

Shapiro-Wilk normality test<br>

data:  v<br>
W = 0.41383, p-value < 2.2e-16

[1] 4.761697<br>
[1] 5.10897<br>
[1] 1.072931<br>

<b>Statistics of gemini-3.5-flash 2026-06-09 08:05:00 in R:</b>

<b>7 42 3000 12</b><br>
con=file("means_3000t_1r_12s_raw_1x3000_12-8x8-7-42", "rb");<br>
v<-c(readBin(con,"double",3000,size=4))<br>
shapiro.test (v)<br>
par(mfrow=c(1,1))<br>
d <- density(v)<br>
plot(d)<br>
rez <- t.test(v, conf.level=0.9999)<br>
ci <- rez$conf.int<br>
ci[1]<br>
ci[2]<br>
ci[2]/ci[1]<br>

Shapiro-Wilk normality test

data:  v<br>
W = 0.85897, p-value < 2.2e-16<br>

[1] 3.19098<br>
[1] 3.240575<br>
[1] 1.015542<br><br>&nbsp;
