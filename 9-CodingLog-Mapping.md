# Week [X] Learning Log

**Student Name:** Emma Stewart
**Week of:** April 20-29   
**Topic(s):** Mapping

---

## What I Worked On This Week

**Assignment(s):**
- [x] Worksheet [9]
- [ ] Other: [describe]

**AI tools used this week:**
- [ ] ChatGPT
- [x] Claude
- [ ] GitHub Copilot
- [ ] Other: [specify]
- [ ] Did not use AI this week

---

## Challenges & Problem-Solving

### Challenge 1: Installation of package issue 

**What I was trying to do:**
I was trying to get the sf package to install on my machine so that I could use it for mapping. 

**What went wrong:**
I kept getting errors and the package would not complete downloading. 

**Did you use AI to troubleshoot this challenge?** Yes

---

#### If YES, I used AI:

**My prompt to AI:**
```
what does this error mean install.packages("sf") :
  installation of package ‘sf’ had non-zero exit status
```

**AI's response:**
This means the sf package failed to install. It's likely missing system dependencies. The sf package requires GDAL, GEOS, and PROJ libraries.

On macOS, install dependencies via Homebrew first:

brew install gdal geos proj

**How I evaluated the AI's suggestion:**
I attempted to do what Claude suggested to see if it would work. 

**What I implemented and why:**
I tried it, but I still could not get the package to download. 


**What I rejected and why:**
See above

**Additional resources I consulted:**
- [ ] Documentation for [package/function]
- [ ] Stack Overflow: [describe]
- [ ] Course materials: [which ones]
- [ ] Slack discussion
- [X] Office hours
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
I asked Dr. Regan for help with this during office hours. She was able to install the dependencies and we finally got it to download. 

**What I learned:**
AI was somewhat helpful here, because it told me the correct dependencies to install. I think the issue was my own error of trying to install them incorrectly. I learned how to do this more efficiently in the future. 

**Verification:**
I was able to install and use the package. 

---

### Challenge 2: Nothing showing up on leaflet plot

**What I was trying to do:**
I was trying to map the gayguides data with leaflet

**What went wrong:**
Nothing would show up on the plot when I ran my code

**Did you use AI to troubleshoot this challenge?** Yes 

---

#### If YES, I used AI:

**My prompt to AI:**
```
What is wrong with this code: leaflet(data=gayguides) %>% addTiles() %>% addMarkers(~lat, ~lon, popup=paste("This location falls into the ", gayguides$type, "category." sep=""))
```

**AI's response:**
Looking at line 283, there are two issues with this code:

Missing comma in paste(): There's a missing comma before sep="". It should be:

Wrong parameter order in addMarkers(): Leaflet expects (lng, lat) order, not (lat, lon). The first parameter should be longitude. It should be: 
leaflet(data=gayguides) %>% addTiles() %>% addMarkers(~lon, ~lat, popup=paste("This location falls into the ", gayguides$type, "category.", sep=""))

**How I evaluated the AI's suggestion:**
This still did not work, so I asked why nothing was showing up. AI suggested that I filter down to one year of the data. 

**What I implemented and why:**
I tried filtering down to one year. 

**What I modified and why:**
I did not have to modify AI's answer because it was more of a general suggestion. 

**What I rejected and why:**
See above. 

**Additional resources I consulted:**
- [ ] Documentation for [package/function]
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
Filtering down to one year of the data worked. 

**What I learned:**
I realized that I was trying to plot way too many years onto leaflet. I am not sure if there is a way to do so, but filtering down might be the main way to go about this function. 

**Verification:**
I double checked that the plot was working and showing the information I wanted it to. 

---

## Reflection

**What I understand well now:**
I feel really good about using mapping tools now! I am excited to use these on my own data when it is ready. 

**What I'm still confused about:**
While I feel good about geocoding and ggmap, I am still figuring out leaflet and how it works. 

**How AI affected my learning this week:**
AI was mostly helpful this week in helping me identify small errors rather than spending hours troubleshooting. 

**Evolving AI strategy:**
As I have stated previously, I feel pretty good about how I phrase questions to AI. I am still figuring out how to evaluate its responses, however, and figuring out if AI is helpful for the specific issue I have. I think it is always best to talk to another person if I continue having trouble. 

**Connection to historical research:**
This week we learned how to map in R. This has numerous connections to historical research, particular for me. I hope to map lesbian separatist communities in the future to see change over time. 

