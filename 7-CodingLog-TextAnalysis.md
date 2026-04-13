# Week [X] Learning Log

**Student Name:** Emma Stewart 
**Week of:** 4/6-4/13 
**Topic(s):** Text Analysis: Tokenization, Stop words, etc

---

## What I Worked On This Week

**Assignment(s):**
- [x] Worksheet 7
- [ ] Other: [describe]

**AI tools used this week:**
- [ ] ChatGPT
- [ ] Claude
- [x] GitHub Copilot
- [ ] Other: [specify]
- [ ] Did not use AI this week

---

## Challenges & Problem-Solving

### Challenge 1: [Brief descriptive title]

**What I was trying to do:**
I was trying to combine the Mind and Body metadata and text into one dataframe. 

**What went wrong:**
Because the metadata and text dfs did not have the same formatting for their file name/doc id, I wasn't sure how I could combine the two; left_join would not work here because none of the columns matched up. 

**Did you use AI to troubleshoot this challenge?** [Yes / No] Yes

---

#### If YES, I used AI:

**My prompt to AI:**
```
I highlighted the dfs and wrote "How can I combine these into one dataframe" 
```

**AI's response:**
```r
metadata <- read.csv("https://raw.githubusercontent.com/regan008/8510-TextAnalysisData/main/mb-metadata.csv")

mb <- readtext(paste(getwd(), "/txt/*.txt", sep=""))

# Sort metadata to match the order of mb
metadata <- metadata %>% arrange(Filename)

# Join them together
mb.whole <- left_join(metadata, mb, by = "doc_id")
```

**How I evaluated the AI's suggestion:**
I knew that this would not work considering the two dfs did not have a column that matched. 

**What I implemented and why:**
I did not implement this at all because it was the wrong way to merge. 

**What I modified and why:**
Instead of using this code, I went back and referred to the way that the metadata and text dfs were combined for the state of the union data. Using this method, I first sorted the dataframes into descending order by the filename and doc id, respectively. Then, I used column bind to paste the two together. This is a precarious method, as you have to make sure both dataframes are in the same order first, but it worked in this instance. 

**What I rejected and why:**
The entire suggestion was wrong. 

**Additional resources I consulted:**
- [x] Documentation for colbind, left join
- [ ] Stack Overflow: [describe]
- [x] Course materials: Notes, worksheet 
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
Using column bind worked. 

**What I learned:**
Here, AI was less than helpful as it told me to do something I had already tried and I knew would not work. 

**Verification:**
See above. 

---

### Challenge 2: [Brief descriptive title]

**What I was trying to do:**
I was trying to load the Women Citizen text files into a dataframe

**What went wrong:**
Each time I tried, I received the error: Error in list_files(file, ignore_missing, TRUE, verbosity) : 
  File '' does not exist.

**Did you use AI to troubleshoot this challenge?** yes

---

#### If YES, I used AI:

**My prompt to AI:**
```
Why am I getting this error: Error in list_files(file, ignore_missing, TRUE, verbosity) : 
  File '' does not exist.
```

**AI's response:**
The issue is that readtext() can't find the files at that path. The problem is likely that when you unzipped the file, it didn't create a TheWomanCitizen/txt/ folder structure.

**How I evaluated the AI's suggestion:**
This was helpful, as I realized that I must be calling the folder and files incorrectly. Still, I wasn't sure how to properly do it. 

**What I implemented and why:**
I did not implement anything AI suggested because it did not give me specific code but told me why mine wasn't working. 

**What I modified and why:**
See above. 

**What I rejected and why:**
See aboce. 

**Additional resources I consulted:**
- [ ] Documentation for 
- [ ] Stack Overflow: [describe]
- [x] Course materials: Worksheet, notes
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
I finally figured out how to fix the code. First, I went to the folder and copied the relative path. Then, I pasted that into my code and it worked. 

**What I learned:**
I learned more about how to read files into a dataframe and how to use proper relative paths. 

**Verification:**
I ran the code and then double checked that the data frame actually represented the files I wanted it to. 

---

## Reflection

**What I understand well now:**
I have a better grasp on how to tokenize and remove stop words from my dataframes.

**What I'm still confused about:**
I am still a bit fuzzy on how to create dataframes out of text files, but I understand this a bit better now. Additionally, I am still figuring out how to create visualizations out of this information, but I think we will cover that more in the coming weeks. 

**How AI affected my learning this week:**
AI was somewhat helpful this week. Most of my questions were not necessarily answered by AI, but it did point me in the right direction or show me what was wrong with me code for the second issue.

**Evolving AI strategy:**
I think I am getting better at determining if AI has a suggestion that will actually help me or not. I am also able to spot when it is feeding me something that doesn't make any sense, especially as I get better at reading code. 

**Connection to historical research:**
This week's lesson has very tangible uses for historical research. Being able to track the raw frequencies of words as well as the tf-idf scores is helpful for figuring out what the main themes of sources were and how they changed over time. 

