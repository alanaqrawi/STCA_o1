# Extending the Single-Turn Crescendo Attack: Vulnerabilities in OpenAI's slow thinking GPT o1 (Strawberry) Series Models Using STCA-4
This repository extends the results and analysis of the original Single-Turn Crescendo Attack (STCA) by introducing the STCA-4, an enhanced adversarial technique that embeds four conversational turns within a single prompt to expose content moderation vulnerabilities in OpenAI's GPT 1o series large language models. (LLMs). 

# Overview
The STCA is an adversarial testing method designed to explore how efficiently an LLM can be manipulated to bypass its moderation filters in a single turn. Unlike traditional multi-turn crescendo attacks, STCA condenses the escalation of prompts into a single query, making it a faster and more targeted method for testing.

This repository includes:

- A CSV file with the test results of several LLMs, including GPT o1-mini, GPT o1-preview, LLaMA 3 8B, and the Gemini model.
- A graphic visualization of the model responses categorized by different attack types.
- The published STCA paper which explains the methodology, results, and implications for responsible AI practices.

Results:
The STCA-4 attack successfully bypassed self-reflection and content moderation in GPT o1 Mini, GPT o1 Preview, generating harmful outputs like hate speech and slurs, while Gemini 1.5 and LLaMA 3 8B consistently resisted the attack. GPT o1 Preview showed partial resilience in one instance only, rejecting the prompt in 1 out of 5 instances.



# Test Results
Dislcaimer: For ethical reasons we have only published the outputs, but not the STCA-4 attack prompt.

The CSV file stca_results.csv contains the following columns: https://github.com/alanaqrawi/STCA_o1/blob/main/stca_results.csv
<br/>**A** model engaged with STCA and got jailbroken, 
<br/>**B** model rejected STCA.

# Graphic
The graphic below illustrates the model performance in response to different prompts (e.g., profanity vs. misinformation). It compares the rate of jailbreaks vs model punts.
!(STCA_o1.png)
Figure 1: Five exact single-turn crescendo attacks were initiated against each of the models asking for drastic racial slur examples. We specifically applied a STCA-4 attack.

# Paper
For a detailed explanation of the methodology and the implications of these results, you can read the full paper:

STCA-o1 Paper:
STCA Paper: https://arxiv.org/abs/2409.03131

# License
This repository is licensed under the CC BY-NC 4.0 License, meaning it is open for non-commercial use. Please contact us for commercial use inquiries.


