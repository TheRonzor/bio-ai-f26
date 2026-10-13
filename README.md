# AI Tips for Biology Students

Prepared for BIOL 601: Introduction to Graduate Studies

October 14, 2026

Each of the prompt examples are provided as markdown files. Markdown is a plain-text and very lightweight language used to format documents. LLMs understand it very well, and it generally minimizes token usage when ingested by an LLM, as compared to formats such as .docx or .pdf which reuqire additional work for the LLM to parse and ingest.

## Contents

### Literature Search / Review

[literature-review.md](literature-review.md)

I've used several variations of prompts like this one for tasks ranging from actual literature review to reviewing multiple college websites for curricular information. Results are generally very good when using an upper-tier frontier model. 

Watch out for hallucinated references, but I haven't noticed any occurences of this since ~GPT 5.6 or so. Part of the prompt also instructs the LLM to create a .csv file with references. A good follow up would be to give that .csv back to the LLM and ask it to verify.

### Reviewing Papers
[paper-review.md](paper-review.md)

A generic prompt for reviewing a paper. Recommend using an upper-tier frontier model for tasks like this.

[paper-review-followup.md](paper-review-followup.md)

When asked to provide critiques and identify errors, LLMs might overdo it a bit (they are, ultimately, conversation continuers). As such, this prompt asks the LLM to critique its own review from the previous prompt. After this, I would feel fairly confident that the response is ready for me to look more closely. Alternatively, skip this step and save some tokens!

### Creating Handoff Documents

[handoff.md](handoff.md)

On a very simplistic level, LLMs use all of the tokens in their context window to predict the next token. Context windows are finite (although they can be quite large these days). Thus, over very long chats you might notice a sudden decline in quality as if the model is starting to forget things you just discussed. This problem becomes worse and happens more quickly with smaller/cheaper models. The purpose of a handoff document is to create a compact representation of the important parts of your chat, so that you can start a fresh chat with a fresh context window and not have to waste time re-explaining yourself.

### Learning How to Code

[programming-1.md](programming-1.md)

[programming-2.md](programming-2.md)

These prompts were written for students of mine learning Python. Just replace "Python" with your language of choice (R, perhaps). The intended usage is to provide a small (or large!) snippet of code with the prompt. These types of tasks typically do not require the latest and greatest LLM, but I would avoid free models unless the code is very basic and not related to a niche application.





