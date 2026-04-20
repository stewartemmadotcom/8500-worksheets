# Week [X] Learning Log

**Student Name:** [Your name]  
**Week of:** [Date range]  
**Topic(s):** [e.g., "Data Visualization with ggplot"]

---

## What I Worked On This Week

**Assignment(s):**
- [X] Worksheet [8]
- [ ] Other: [describe]

**AI tools used this week:**
- [ ] ChatGPT
- [X] Claude Haiku 4.5 
- [ ] GitHub Copilot
- [ ] Other: [specify]
- [ ] Did not use AI this week

---

## Challenges & Problem-Solving

### Challenge 1: [Brief descriptive title]

**What I was trying to do:**
I wanted to graph only the gamma values of topic #20 instead of all of them. 

**What went wrong:**
I could not figure out how to only graph that one topic. 

**Did you use AI to troubleshoot this challenge?** Yes 

---

#### If YES, I used AI:

**My prompt to AI:**
```
how do I filter this to only plot one of my topics
```

**AI's response:**
```r
ggplot(data=mb.1930 %>% filter(topic == 23), aes(x=issue_date, y=gamma)) + 
  geom_bar(stat="identity") + 
  theme(axis.text.x = element_text(angle = 90, vjust = 0.5, hjust=1))
```

**How I evaluated the AI's suggestion:**
This response helped me figure out that I could simply filter for one of my topics. 

**What I implemented and why:**
I decided to separately filter for topic 20 and save that as a new df. 

**What I modified and why:**
I broke up the suggested code into chunks so that I could better understand what I was doing. 

**What I rejected and why:**
The suggestion was fine, but I decided not to filter the data in the same line I graphed it. 

**Additional resources I consulted:**
- [X] Documentation for LDA()
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
I figured it out and used filter to only plot one of the topics. 

**What I learned:**
I now have a better understanding of how topic modeling works and how I can manipulate the data. 

**Verification:**
I double checked by running the graph, which only gave me one topic, and then verifying that the editions with high gamma values actually aligned with the topic I wanted to graph. 

---

### Challenge 2: [Brief descriptive title]

**What I was trying to do:**
I was trying to find a good number of topics for the American City data. 

**What went wrong:**
All of my topics looked the exact same. 

**Did you use AI to troubleshoot this challenge?** No

---

#### If YES, I used AI:

**My prompt to AI:**
```
[Copy your exact prompt here]
```

**AI's response:**
```r
# Paste the relevant code or explanation AI provided -- this can brief and abbreviated or summarized if the response is long.
```

**How I evaluated the AI's suggestion:**

**What I implemented and why:**
[Which parts of the AI's suggestion were appropriate?]

**What I modified and why:**
[What did you change? Why was the change necessary?]

**What I rejected and why:**
[What suggestions did you not use? Why were they inappropriate?]

**Additional resources I consulted:**
- [ ] Documentation for [package/function]
- [ ] Stack Overflow: [describe]
- [ ] Course materials: [which ones]
- [ ] Slack discussion
- [ ] Office hours
- [X] Other: Tech Table and conversation with classmate 

---

#### If NO, I didn't use AI:

**Why I chose not to use AI:**
I did not think that AI would have a good answer for me and simply decided not to use it. I felt like my problem was more fundamental that a quick fix. 

**My problem-solving process:**
1. I tried to expand my number of topics incrementally to see if that provided better results. 
2. I sat with Sharon and worked through different numbers of topics with her. 
3. Finally, Dr. Regan told us to try using the Gibbs method, and it worked much better. 

**Resources I consulted:**
- [ ] Documentation for [package/function]
- [ ] Stack Overflow: [describe what you searched for]
- [ ] Course materials: [which ones]
- [ ] Slack discussion
- [ ] Office hours
- [X] Classmate, Tech Table 

---

**Resolution:**
The issue was that we were not using the Gibbs method; after adding that in, the topics were much more decipherable. 

**What I learned:**
I should make sure to double check my notes next time to see if I am missing anything. Sometimes, it is a quick fix. 

**Verification:**
I ran the topic models with the Gibbs method and they made much more sense. 

---

## Reflection

**What I understand well now:**
I feel really good about topic modeling now, especially after doing so much troubleshooting on my second problem. I feel like I am figuring out how to hone in on the correct number of topics. 

**What I'm still confused about:**
I think the gamma and beta values are still a little bit challenging to wrap my head around, but I should be able to rememdy this through re-reading my notes and documentation. 

**How AI affected my learning this week:**
AI helped me figure out how to filter my data down, which was a pretty simply problem.  

**Evolving AI strategy:**
I think that I only really find AI helpful for very concrete and simple answers. If there is something more meaningful going wrong, it is better to read up on the issue or ask for help. 

**Connection to historical research:**
Topic modeling has really impressed me as a potential research tool. I am really excited to use this method on my own data, once I have a textual dataset, and find where specific discourse happens in the corpus. 

