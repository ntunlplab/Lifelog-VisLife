# VisLife [viz laɪv]: Visual Lifelogging Dataset

Personal Knowledge Base Construction from Multimodal Data
# Introduction
Recently, people tend to record their daily life via filming Video Weblog (VLog), which contains visual and audio data. These large scale multimodal data can be used to support information recall service that enables users to query their past experiences. To this end, we construct a visual lifelogging dataset for investigating the issues of personal life event extraction from vlogs shared on YouTube and constructing a personal knowledge base (PKB) for individuals. There are 1,733 videos from three selected YouTubers ranging from 2016 to 2019. The videos we crawled are all about traveling.

# Format
Each row of the csv files is consisted of video_id, list of action, list of video clip length and the path to the triple file.

The entry in the triple JSON format is composed of "subject", "verb", "object", "times", and "subtitle" of each life event.

The triple_mapping and verb_and_object_mapping provide the id of class (the id pair of verb and object).

# Example
#### train.csv
    
```
    id, actions, length, path
    a2xDIcRUQ_I, c0000 13.2 53.2;c0001 206.33 246.33, PATH_TO_TRIPLE/CHANNEL_NAME/DATE/VIDEO_NAME/triples.json
    ...
```

#### triples.json
```yaml
    {
        "subject": {
          "50": "i",
          ...
        },
        "verb": {
          "50": "finish",
          ...
        },
        "object": {
          "50": "pancakes",
          ...
        },
        "times": {
          "50": "569.53",
          ...
        },
        "subtitle": {
          "50": "I'M gonna fall asleep on the bikes down,
                and this is how I feel when I can't finish the best pancakes in the world,
                but I did get a doggie bag and also I have one final wish yo.",
          ...
        }
      }
```
   
#### triple_mapping.json
```yaml
    
    {
        "c0420": ["v0019", "o0115"],
        ...
    }
```
  
#### verb_and_object_mapping.json
```yaml
   
    {
        "c0420": ["get", "food"],
        ...
    }
```
    
# Download
Please write us an email with the agreement. Click here to download the agreement of VisLife.

Email Address: azyen@nlg.csie.ntu.edu.tw

# How to Cite the Corpus
Please cite the following papers when referring to the VisLife in academic publications and papers.

An-Zi Yen, Chia-Chun Chang, Hen-Hsen Huang, and Hsin-Hsi Chen (2021). “Personal Knowledge Base Construction from Multimodal Data.” In Proceedings of ACM International Conference on Multimedia Retrieval 2021 (ICMR 2021), August 21-24, 2021, Taipei, Taiwan.
DOI:
# License
VisLife is made available under the Creative Commons Attribution 4.0 International (CC BY 4.0) license.
