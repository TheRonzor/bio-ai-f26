# AI/LLM Tips and Example Prompts for Biology (and in general)

Prepared for BIOL 601: Introduction to Graduate Studies

Presented on: October 14, 2026

Each of the prompt examples is provided as a Markdown file. Markdown is a plain-text and very lightweight language used to format documents. LLMs understand Markdown very well, and its lightweight formatting generally makes it easier to process than formats such as .docx or .pdf, which may require additional parsing or conversion by the LLM.

## Contents

### Literature Search / Review

[literature-review.md](literature-review.md)

I've used several variations of prompts like this one for tasks ranging from actual literature review to reviewing multiple college websites for curricular information. Results are generally very good when using an upper-tier frontier model. 

Watch out for hallucinated references, but I haven't noticed any occurrences of this since ~GPT 5.6 or so. Part of the prompt also instructs the LLM to create a .csv file with references. A good follow-up would be to give that .csv back to the LLM and ask it to verify the references.

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

These prompts were written for students of mine learning Python. The goal is to use the LLM as your own personalized tutor. Just replace "Python" with your language of choice (R, perhaps). The intended usage is to provide a small (or large!) snippet of code with the prompt. These types of tasks typically do not require the latest and greatest LLM, but I would avoid free models unless the code is very basic and not related to a niche application.

### Using Persistent Agent Instructions

[AGENTS.md](AGENTS.md)

I primarily use [Codex](https://chatgpt.com/codex/) for more complex tasks. Codex is an "agent proper", meaning that it is more than just an LLM - it is an application you install on your computer, has access to your files/folders, and can be granted varying levels of permissions to directly work on your behalf.

Codex will specifically look for an AGENTS.md file in your project directory and, if present, will automatically incorporate those instructions into its work. Tools by other vendors have a similar feature. For example, Anthropic's Claude Code uses a CLAUDE.md file for similar purposes.

This version is a very general set of instructions I have used for a variety of projects such as:

- Websites
- Research projects
- Lesson planning
- Curricular development
- Personal projects, such as a Fantasy Football website for myself and friends

Its main features are:

- The agent is instructed to keep detailed documentation about project decisions, findings, and future directions at all times
- The documentation it creates is compartmentalized by topic (e.g., research logs, style guides, and project-specific workflows). The agent is instructed to only reference the documentation it needs when it needs it, i.e., do not waste tokens reading irrelevant documents.
- It emphasizes data validation and, especially, thorough testing of code.
- The documentation it maintains should be complete. It should not be necessary to ever re-explain any aspects of the project when you move to another computer or share the project with someone else.

This is intended for use with complex, multi-step projects. In those cases, it will likely result in a more efficient use of the LLM in terms of token consumption. It should not be used with simpler projects, as the documentation and testing protocols will likely result in a larger token spend. The instructions can and should be modified on a project-specific basis to keep it efficient. For example, there's no need to have the agent run detailed tests on "simpler" code that you could easily test yourself.

### Go Caveman

Funny as it may sound, if you want to minimize token usage and "save" the environment while still allowing yourself to use LLM tools, check out the [Caveman](https://github.com/juliusbrussee/caveman). As the intro says,

> "why many token when few do trick"

The way it is presented in the linked repository may make it look more complicated to implement than it actually is. You don't need to install anything, and you can easily write an instruction like this yourself in a simple Markdown file. The basic idea is to instruct the agent to avoid non-informative words in its replies.

This isn't a joke. Claude Shannon's 1951 paper, [Prediction and Entropy of Printed English](https://www.princeton.edu/~wbialek/rome/refs/shannon_51.pdf), estimates that written English is approximately 75% redundant in an information-theoretic sense. In other words, much of what we write is statistically predictable from what came before it, and therefore carries relatively little _new_ information.