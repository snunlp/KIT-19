# KIT-19: A Comprehensive Korean Instruction Toolkit on 19 Tasks for Fine-Tuning Korean Large Language Models

## Access to KIT-19 on Huggingface

For ease of access and to facilitate research and development, the KIT-19 dataset and the fine-tuned models are also hosted on Huggingface. Please use the following links to explore and utilize these resources:

### KIT-19 Dataset 🤗
- [KIT-19 Instruction Dataset](https://huggingface.co/datasets/Junmai/kit-19-instruction-100000)

### Fine-tuned Models 🤗
- [KIT-1.3b Model](https://huggingface.co/Junmai/KIT-1.3b)
- [KIT-5.8b Model](https://huggingface.co/Junmai/KIT-5.8b)

These resources are available for the community to further Korean NLP research and applications. We encourage their use in your projects and research endeavors.

## Introduction

In the current landscape of language models, achieving high performance in Korean NLP tasks requires specialized instruction datasets tailored to the unique aspects of the Korean language. To address the scarcity of such datasets, we introduce **KIT-19**, a comprehensive Korean Instruction Toolkit that encompasses 19 distinct tasks for fine-tuning Korean Large Language Models (LLMs). Unlike existing datasets that largely rely on translated instructions or outputs from models like ChatGPT, KIT-19 is meticulously crafted to capture the nuances of Korean language and culture, offering a robust foundation for advancing Korean LLMs.

## Overview of KIT-19 Datasets

KIT-19 amalgamates 19 existing open-source datasets, each converted into an instruction format to facilitate instruction tuning for Korean LLMs. Here's a brief overview of the datasets included in KIT-19:

| Task Category                         | Datasets Included                                                                                        |
|---------------------------------------|----------------------------------------------------------------------------------------------------------|
| Hate Speech Detection                 | APEACH, UnSmile, HateScore                                                                               |
| Boolean Question Answering (QA)       | KoBEST\_BoolQ                                                                                            |
| Natural Language Inference (NLI)      | KoBEST\_COPA, korNLI                                                                                     |
| Text Generation                       | KoBEST\_HellaSwag, kowiki\_text                                                                          |
| Semantic Textual Similarity (STS)     | korSTS, pawsx\_paraphr, ParaKQC, KoBEST\_WIC, Style\_KQC, Question\_Pair                                 |
| Sentiment Analysis (SA)               | NSMC                                                                                                     |
| Intent Argument Extraction            | sae4k\_sum, petitions\_archive                                                                           |
| Math                                  | math\_korean                                                                                             |
| Closed Book QA                        | kowiki\_text (utilized differently for Closed Book QA and Text Generation)                              |
| Summarization                         | lbox\_summarization                                                                                      |

_Each dataset is selected and formated to ensure a wide coverage of tasks and scenarios relevant to the Korean language, making KIT-19 an exhaustive resource for developing and fine-tuning Korean LLMs._

## Fine-Tuned Models

To demonstrate the effectiveness of KIT-19, we have fine-tuned representative Korean Pretrained LLMs, including Polyglot-Ko-5.8b and Polyglot-Ko-1.3b. The fine-tuned models showcase significant performance improvements across a variety of benchmark datasets:

- KoBEST\_COPA
- KoBEST\_BoolQ
- KoBEST\_HellaSwag
- KLUE\_STS
- KoBEST\_SentiNeg
- KLUE\_YNAT

The experimental results affirm that **models trained with KIT-19 significantly outperform existing Korean LLMs**, highlighting the potency and necessity of instruction datasets crafted specifically for the Korean language.

# Benchmark Performance

Below is the performance comparison of different models on various benchmark datasets. The models trained with KIT-19 (KIT-5.8b and KIT-1.3b) are compared against Polyglot-Ko-1.3b, Polyglot-Ko-5.8b, KoAlpaca-5.8b, and Kullm-polyglot-5.8b-v2.

| Benchmark Dataset        | Metric      | Polyglot-ko-1.3b | Polyglot-ko-5.8b | KoAlpaca-5.8B | kullm-polyglot-5.8b-v2 | KIT-5.8b       | KIT-1.3b       |
|--------------------------|-------------|------------------|------------------|---------------|------------------------|----------------|----------------|
| KoBEST\_COPA             | ACC         | 72.00%           | 77.60%           | 69.80%        | 76.60%                 | **91.60%**     | 83.80%         |
|                          | F1 (macro)  | 71.96%           | 77.55%           | 69.77%        | 76.53%                 | **91.59%**     | 83.78%         |
| KoBEST\_BoolQ            | ACC         | 49.86%           | 53.63%           | 56.34%        | 50.28%                 | **66.24%**     | 50.71%         |
|                          | F1 (macro)  | 35.52%           | 43.56%           | 50.64%        | 33.71%                 | **66.14%**     | 34.78%         |
| KoBEST\_HellaSwag        | ACC         | 40.60%           | 48.80%           | 38.20%        | 44.40%                 | **97.60%**     | 81.60%         |
|                          | ACC\_Norm   | 53.00%           | 59.80%           | 46.20%        | 55.20%                 | **98.20%**     | 89.80%         |
|                          | F1 (macro)  | 40.13%           | 48.53%           | 38.15%        | 44.25%                 | **97.61%**     | 81.49%         |
| KLUE\_STS                | ACC         | 42.39%           | 45.28%           | 51.83%        | 42.39%                 | **65.51%**     | 42.20%         |
|                          | F1          | 59.54%           | 60.34%           | 33.86%        | 59.54%                 | **69.71%**     | 56.52%         |
| KoBEST\_SentiNeg         | ACC         | 69.27%           | 50.38%           | 38.79%        | 50.38%                 | 71.54%         | **80.86%**     |
|                          | F1          | 68.19%           | 33.95%           | 38.48%        | 33.50%                 | 68.98%         | **80.86%**     |
| KLUE\_YNAT               | F1          | 33.24%           | 33.62%           | 20.91%        | 32.20%                 | 28.15%         | **38.34%**     |

*Bold* results indicate the best performance in each category.

## Conclusion and Future Work

KIT-19 stands as a pivotal development in the Korean NLP landscape, addressing the critical need for comprehensive instruction datasets that encapsulate the linguistic and cultural intricacies of the Korean language. With KIT-19, we aim to push the boundaries of what's possible with Korean LLMs, laying a solid foundation for future advancements in the field.

We are committed to continuously expanding KIT-19 to cover more domains and further enhance the generability of Korean LLMs. Our hope is that KIT-19 not only serves as a valuable resource for NLP practitioners but also inspires further research and development within the Korean NLP community.

_The KIT-19 dataset and the fine-tuned models are publicly available for research and development purposes, fueling advancements in Korean language modeling and applications._

---

For more information, access to the datasets, and models, please visit our [GitHub repository](https://github.com/qwer4107/kit-19).

**Contributors:** Dongjun Jang, Sungjoo Byun, Hyemi Jo, Hyopil Shin from the Department of Linguistics, Seoul National University

_This work is supported by the linguistic insights and technological advances in NLP and aims to contribute to the broader academic and practical applications of language models._
