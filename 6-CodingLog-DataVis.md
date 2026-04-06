# Week [] Learning Log

**Student Name:** Emma Stewart
**Week of:** March 30 - April 6
**Topic(s):** Data Visualization, ggplot 

---

## What I Worked On This Week

**Assignment(s):**
- [X] Worksheet [6]
- [ ] Other: [describe]

**AI tools used this week:**
- [ ] ChatGPT
- [ ] Claude
- [X] GitHub Copilot
- [ ] Other: [specify]
- [ ] Did not use AI this week

---

## Challenges & Problem-Solving

### Challenge 1: [Brief descriptive title]

**What I was trying to do:**
I was trying to answer this prompt:
> Using the state recreation data, can you create a chart that outlines the total expenditures in South Carolina by city?

**What went wrong:**
When I used ggplot with geom_line and facet wrap, nothing showed up on my graph. 

**Did you use AI to troubleshoot this challenge?** [Yes / No] Yes

---

#### If YES, I used AI:

**My prompt to AI:**
```
Why is this not showing anything
```
> I thought this would be a simple troubleshootint issue due to incorrect formatting, so my question was not very specific. 
**AI's response:**
```r
sc.rec <- recreational.data %>% 
  filter(state == "SC") %>%
  group_by(city) %>%
  summarize(total_exp = sum(total_expenditures))

ggplot(sc.rec, aes(x = city, y = total_exp)) + 
  geom_col()
```
> AIs explanation: The issue is that geom_line() needs multiple points per city to draw a line, but your current data structure likely has only one row per city. Since the question asks to show total expenditures in South Carolina by city, use a bar chart instead:

**How I evaluated the AI's suggestion:**
 All AI recommended was to change to a bar chart. 
**What I implemented and why:**
I went ahead and changed to a bar graph, which made more sense because I was only plotting one piece of data for each row.

**What I modified and why:**
[What did you change? Why was the change necessary?]

**What I rejected and why:**
[What suggestions did you not use? Why were they inappropriate?]

**Additional resources I consulted:**
- [X] Documentation for [package/function]
- [ ] Stack Overflow: [describe]
- [ ] Course materials: [which ones]
- [ ] Slack discussion
- [ ] Office hours
- [ ] Other: [describe]


echo 'eval "$(/opt/homebrew/bin/brew shellenv)"' >> ~/.zprofile
eval "$(/opt/homebrew/bin/brew shellenv)"
---

#### If NO, I didn't use AI:

**Why I chose not to use AI:**
[Explain your reasoning - wanted to understand it myself, AI struggles with this type of problem, etc.]

**My problem-solving process:**
1. [First attempt - what you did and what happened]
2. [Second attempt - what you did and what happened]
3. [Additional attempts if relevant]

**Resources I consulted:**
- [ ] Documentation for [package/function]
- [ ] Stack Overflow: [describe what you searched for]
- [ ] Course materials: [which ones]
- [ ] Slack discussion
- [ ] Office hours
- [ ] Other: [describe]

---

**Resolution:**
Using the column plot worked pretty well for this problem, although I am not 100% sure if I answered the question correctly. 

**What I learned:**
Although it seems obvious, I need to take more care in picking what plot I use. Each one has a particular use case and will not work right for the wrong data. 

**Verification:**
I tested the code by running it and checking the visualization. Additionally, this was such a small fix I knew that the code was correct (because I have multiple examples of that exact code). 

---

### Challenge 2: [Brief descriptive title]

**What I was trying to do:**
I wanted to put two plots next to each other, but the plots used different data so I did not think faceting would work. 

**What went wrong:**
I was unsure of how to show two different graphs side by side. 

**Did you use AI to troubleshoot this challenge?** [Yes / No] Yes 

---

#### If YES, I used AI:

**My prompt to AI:**
```
how would I do two ggplots with different data next to each other
```

**AI's response:**
```r
library(patchwork)

plot1 <- ggplot(data1, aes(x = var1, y = var2)) + geom_point()
plot2 <- ggplot(data2, aes(x = var3, y = var4)) + geom_line()

plot1 | plot2
```
> AI recommended I install patchwork and then showed me the formatting. 

**How I evaluated the AI's suggestion:**
I looked up the documentation for patchwork and learned that it is a ggplot package that allows for multiplot layouts (exactly what I was looking for). 

**What I implemented and why:**
I downloaded patchwork because it seemed like a simple way to get my plots side by side. 

**What I modified and why:**
AI offered some alternative steps that seemed less useful for this use case. It recommended gridExtra as well, but that seemed to be more complicated than what I needed. 

**What I rejected and why:**
[What suggestions did you not use? Why were they inappropriate?]

**Additional resources I consulted:**
- [X] Documentation for [package/function]
- [ ] Stack Overflow: [describe]
- [ ] Course materials: [which ones]
- [ ] Slack discussion
- [ ] Office hours
- [ ] Other: [describe]

---

#### If NO, I didn't use AI:

**Why I chose not to use AI:**
[Explain your reasoning - wanted to understand it myself, AI struggles with this type of problem, etc.]

**My problem-solving process:**
1. [First attempt - what you did and what happened]
2. [Second attempt - what you did and what happened]
3. [Additional attempts if relevant]

**Resources I consulted:**
- [ ] Documentation for [package/function]
- [ ] Stack Overflow: [describe what you searched for]
- [ ] Course materials: [which ones]
- [ ] Slack discussion
- [ ] Office hours
- [ ] Other: [describe]

---

**Resolution:**
Using patchwork worked perfectly. 

**What I learned:**
AI did help me figure out quickly how to plot two graphs next to one another despite using different data. However, I think that it is important that, going forward, I continue to check the documentation of the packages AI recommends so I know what they actually do. 

**Verification:**
I tested this code by looking at the documentation and then by running it as a visualization. 

---

## Reflection

**What I understand well now:**
I feel like I have a good grasp on ggplot now, and it has been really exciting to start visualizing data. 

**What I'm still confused about:**
I think I could use more practice with different types of plots and customization of them. I also need to practice more data tidying, as I imagine that will become even more important as we go forward. 

**How AI affected my learning this week:**
AI saved me quite a bit of time this week from googling or missing easily fixed grammatical errors. However, I did not use it too much because I wanted to figure out as much as I could on my own. 

**Evolving AI strategy:**
I think I am still finding the right balance between using AI to make life easier and not using it at all. I am also still working on how to properly word questions to get the desired help. 

**Connection to historical research:**
The ability to visualize data is huge; these ggplots can reveal important historical information very quickly (as compared to sifting through data sets). 

