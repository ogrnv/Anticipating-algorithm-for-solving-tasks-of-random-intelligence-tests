# Anticipating-algorithm-for-solving-tasks-of-random-intelligence-tests


When a LLM solves a complex task of random intelligence tests it as a rule results in infinite loops or infinite wandering. 

In the anticipating algorithm AI should first create a future state of the test board with chips. And then it should come to the state. 
The determination of the future state eliminates the loops or wanderings.

Anticipating algorithm recalls the fragment: "A spider conducts operations that resemble those of a weaver, and a bee puts to shame many an architect in the construction of her cells. But what distinguishes the worst architect from the best of bees is this, that the architect raises his structure in imagination before he erects it in reality." from Karl Marx's Capital. 

This is a example of prompt for the algorithm:

Your code should first rearrange the chips of a given TB to obtain a different optimal TB in which formation of a straight horizontal or vertical or diagonal line of five or more chips with the same marking is completed. 
The code should then make an array of optimal moves i.e. array from-to addresses leading from the given TB to the optimal TB.
The code should then issue as TTSR results x0, y00, x1, y01 from the array, ignoring new input TBs until the step completes.
Optimal means "in accordance with the goal of the test round".
<br><br>
<b>The known best results of intelligence tests of AI-generated code for pv2a.c</b><br>the data was obtained with saving global variables before each call of an AI ​​code and restoring the variables after that:<br><br>
| Grid | NChipT | Chips | Rounds | SinR | **Intelligence** | Model | Region | Timestamp |
|------|------|-------|-------|-----|------------|-------|--------|-----------|
|8×8|7|59|1300|6| **86.998** |gemini-3.5-flash|us|2026-06-29 09:03:00|
|8×8|7|42|3000|12| **310.967** |gemini-3.5-flash|us|2026-06-09 08:05:00|
|8×8|7|59|650|12| **59.399** |gemini-3.5-flash|us|2026-06-09 08:05:00|
|8×8|7|59|1300|6| **54.749** |gemini-3.5-flash|us|2026-06-09 08:05:00|
|8×8|7|42|3000|12| **121.469** |kimi-K3-Max|cn|2026-07-16 18:02:00|
|8×8|7|59|1300|6| **9.030** |kimi-K3-Max|cn|2026-07-16 18:02:00|
<br>
Where:<br>
&nbsp; &nbsp; NChipT - the number of chip types<br>
&nbsp; &nbsp; Chips - chips on the board<br>
&nbsp; &nbsp; Rounds - rounds in a test<br>
&nbsp; &nbsp; SinR -steps in a round<br>
&nbsp; &nbsp; Intelligence = 1000 / average number of moves made per step<br>
&nbsp; &nbsp; Timestamp - date and time of the code generation<br><br>

<b>Statistics of gemini-3.5-flash 2026-06-29 09:03:00 in R:</b>

<b>7 59 10 6</b><br>
con=file("means_1300t_1r_6s_FI130", "rb");<br>
v<-c(readBin(con,"double",1300,size=4))<br>
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
W = 0.74833, p-value < 2.2e-16

[1] 10.50157<br>
[1] 12.4874<br>
[1] 1.189098<br>

<b>Statistics of gemini-3.5-flash 2026-06-09 08:05:00 in R:</b>

<b>7 42 5 12</b><br>
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
[1] 1.015542<br><br>
<b>7 59 5 12</b><br>
con=file("means_650t_1r_12s_FF", "rb");
v<-c(readBin(con,"double",3000,size=4))
shapiro.test (v)
par(mfrow=c(1,1))
d <- density(v)
plot(d)
rez <- t.test(v, conf.level=0.9999)
ci <- rez$conf.int
ci[1]
ci[2]
ci[2]/ci[1]

Shapiro-Wilk normality test

data:  v<br>
W = 0.91612, p-value < 2.2e-16

[1] 15.42219<br>
[1] 18.24832<br>
[1] 1.183251<br><br>
<b>7 59 10 6</b><br>
con=file("means_1300t_1r_6s_F130", "rb");
v<-c(readBin(con,"double",1300,size=4))
shapiro.test (v)
par(mfrow=c(1,1))
d <- density(v)
plot(d)
rez <- t.test(v, conf.level=0.9999)
ci <- rez$conf.int
ci[1]
ci[2]
ci[2]/ci[1]

Shapiro-Wilk normality test

data:  v
W = 0.82961, p-value < 2.2e-16

[1] 16.75112<br>
[1] 19.7794<br>
[1] 1.180781<br>

