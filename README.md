# LLM-Based Clinical Notes Section Identifier

:tada: Exciting News! Our paper titled “LLM-Based Section Identifiers Excel on Open Source but Stumble in Real World Applications” has been accepted at NAACL - Clinical NLP! :tada:
In this paper, we tackle the challenge of navigating through lengthy Electronic Health Records (EHRs) by using Large Language Models (LLMs) to identify semantically relevant sections in increasingly lengthy EHR notes. Our findings show that GPT-4 can effectively solve this task in both zero and few-shot settings, outperforming state-of-the-art methods.
However, when tested on a more challenging real-world dataset, GPT-4's performance falters, indicating the need for further research and harder benchmarks.

### Introduction

In this repository we provide the result of a manual annotation of a dataset in healthcare. This dataset consists of of prior authorization requests derived from faxed-in images being transcribed to text via an optical character recognition system (OCR). These requests contain EHR of patients in the form of doctors’ notes, submitted in both PDF and image formats. These documents lack a standardized structure, with segments and titles that can vary significantly in length. Although it’s possible to group these titles into clusters of similar meaning, the language and number of titles differ across documents. Additionally, OCR inaccuracies arise from unclear text, spelling errors, complex table structures, and handwritten content, resulting in highly noisy input for any Section Identification (SI) system to process. 

Check out the full paper here: https://arxiv.org/abs/2404.16294 
