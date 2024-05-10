# LLM-Based Clinical Notes Section Identifier

:tada: Exciting News! Our paper titled “LLM-Based Section Identifiers Excel on Open Source but Stumble in Real World Applications” has been accepted at NAACL - Clinical NLP! :tada:
In this paper, we tackle the challenge of navigating through lengthy Electronic Health Records (EHRs) by using Large Language Models (LLMs) to identify semantically relevant sections in increasingly lengthy EHR notes. Our findings show that GPT-4 can effectively solve this task in both zero and few-shot settings, outperforming state-of-the-art methods.
However, when tested on a more challenging real-world dataset, GPT-4's performance falters, indicating the need for further research and harder benchmarks.

Check out the full paper here: https://arxiv.org/abs/2404.16294 

## Introduction

In this repository we provide the result of a manual annotation of a dataset in healthcare. This dataset consists of of prior authorization requests derived from faxed-in images being transcribed to text via an optical character recognition system (OCR). These requests contain EHR of patients in the form of doctors’ notes, submitted in both PDF and image formats. These documents lack a standardized structure, with segments and titles that can vary significantly in length. Although it’s possible to group these titles into clusters of similar meaning, the language and number of titles differ across documents. Additionally, OCR inaccuracies arise from unclear text, spelling errors, complex table structures, and handwritten content, resulting in highly noisy input for any Section Identification (SI) system to process. 

## Annotation Design

We randomly selected 100 records from a pool of one million records we have in our corpus. These records are in two forms, PDF or fax images which doctors submit to insurance companies, and hence, can arrive from any arbitrary format. We refer to these records as documents in the span of this manuscript. These documents have no standard structures and sometimes they contain multiple patients information at the same time. Six annotators with higher education and nonnative speakers of English carry the annotation task. Each annotates an equal amount and random selection of these documents. After this phase of annotation, two annotators annotate these sections and sub-sections to more general categories. The purpose of this annotation was to use human expertise with no prior definition or defined categories to create those categories. The results of these annotation were one set of fine-grained labels and one set of coarse-grained labels of categories. We encourage the readers to continue reading the annotation instruction, results, and discussion in our paper which is refrence above. We share the sections and subsections in a CSV file in this respositories. 

Below is a sample of sections and subsections with the highest frequency:

| Info | Instance |
| --- | --- |
| **Medications Section** | Information about the current and past Medications |
| **Order Info** | This section consists of additional items that are required to conclude the assessments. Examples of such items are Mammograms, x-rays, etc., or the information about the provider of such items.  |
| **Results Section** | Usually contains of lab results |
| **Physical Exam Section** | Result of physical exams such as Integumentary, Chest and Lung Exam, Cardiovascular, Abdomen, etc. |

## File Structure

* `sections_subsections.csv` in `resources` folder
  * Section and Subsection Names -> names of section and subsections that are extracted from the documents
  * annotator_1 (coarse-grained catefories) -> coarse-grained categories that are identified by the annotator
  * Annotator_2 (fine-grained catefories) -> fine-grained categories that are identified by the annotator
  * Section/Subsection -> if the extracted item is section or subsection
    
## Contacts

You can send your emails to Saranya Krishnamoorthy, Ayush Singh, Shabnam Tafreshi, emails: firstname.lastname@evicore.com, if you have questions, suggestions, or concerns.

## Citation

```
@article{krishnamoorthy2024llm, <br/>
  title={LLM-Based Section Identifiers Excel on Open Source but Stumble in Real World Applications}, <br/>
  author={Krishnamoorthy, Saranya and Singh, Ayush and Tafreshi, Shabnam}, <br/>
  journal={arXiv preprint arXiv:2404.16294}, <br/>
  year={2024} <br/>
}
```

