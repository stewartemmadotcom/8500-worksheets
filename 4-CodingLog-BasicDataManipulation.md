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

### Challenge 1: Grep vs. Grepl

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

### Challenge 2:  Mutating a column into a factor 

**What I was trying to do:**
I was trying to use mutate to change a column to a factor instead of a character 

**What went wrong:**
When I tried to check the levels of the factor, I was getting NULL in response

**My problem-solving process:**
1. First I double checked my code, but everything seemed right. I rewrote it in a few different ways, and then I realized that I had not saved the function's results to a new dataframe, so I do not think it was actually changing the column/saving a new one. 
2. [Second attempt - what you did and what happened]
3. [Additional attempts if relevant]

**Resources I consulted:**
- [x] Documentation for [package/function]
- [ ] Stack Overflow: [describe what you searched for]
- [x] Course materials: Notes
- [ ] Slack discussion
- [ ] Office hours
- [ ] Other: [describe]

**Resolution:**
I went ahead and saved my function to a data frame, and it worked! 

**What I learned:**
This taught me that the tidyverse functions wont actually change anything unless you tell it where to store the changes/create a new variable/dataframe for it. 

---

## Reflection

**What I understand well now:**
I feel really good about the tidyverse functions we learned this week; I ran into minimal trouble and think I have a good grasp on how to properly use them. 

**What I'm still confused about:**
I think I could use clarification on my second challenge 

**Connection to historical research:**
The skills from this week will come in handy for easier querying of data sets than the use of base R functions. Additionally, this skill set will be built upon next week when we start using the tidyverse to do more tidying of data. 


