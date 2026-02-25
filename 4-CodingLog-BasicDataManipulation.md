# Week [X] Learning Log

**Student Name:** Emma Stewart
**Week of:** 2/23/26-3/2/26
**Topic(s):** Basic Data Manipulation

---

## What I Worked On This Week

**Assignment(s):**
- [x ] Worksheet [4]
- [ ] Other: [describe]

---

## Challenges & Problem-Solving

### Challenge 1: [Brief descriptive title]

**What I was trying to do:**
I was attempting to filter the gayguides data to find all locations that had G or L in the amenity features column using the filter function of the tidyverse. 

**What went wrong:**
I could not figure out how to use grep within the filter function. 

**My problem-solving process:**
1. First, I checked that I knew how to use grep on its own. When I searched for G in the amenityfeatures column without worrying about filter, it worked. Then I tried to integrate it back into the filter function and received an error. 
2. At this point, I realized that grep was trying to return the row numbers that matched my search. It clicked then that I needed to use a function that returned a logical value rather than a row number. 
3. Next I tried grepl instead of grep, and I got it to work! 

**Resources I consulted:**
- [x] Documentation for [package/function]
- [ ] Stack Overflow: [describe what you searched for]
- [ ] Course materials: [which ones]
- [ ] Slack discussion
- [ ] Office hours
- [ ] Other: [describe]

**Resolution:**
Once I figured out that I needed a logical value, I realized that grepl would be better inside the filter function. 

**What I learned:**
This reinforced for me that I need to make sure that I am using logical values with these tidyverse functions! 

---

### Challenge 2: [Brief descriptive title]

**What I was trying to do:**
[Describe the task or problem]

**What went wrong:**
[Describe the error, confusion, or roadblock]

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

**Resolution:**
[What ultimately worked or where you're still stuck]

**What I learned:**
[What did this teach you about the concept, the tool, or problem-solving?]

---

### Challenge 3 (Optional): [Brief descriptive title]

**What I was trying to do:**
[Describe the task or problem]

**What went wrong:**
[Describe the error, confusion, or roadblock]

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

**Resolution:**
[What ultimately worked or where you're still stuck]

**What I learned:**
[What did this teach you about the concept, the tool, or problem-solving?]

---

## Reflection

**What I understand well now:**
[What clicked for you this week?]

**What I'm still confused about:**
[What remains unclear? What questions do you have?]

**Connection to historical research:**
[How might this week's skills apply to your research?]


