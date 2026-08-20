---
# For reference on dataset card metadata, see the spec: https://github.com/huggingface/hub-docs/blob/main/datasetcard.md?plain=1
# Doc / guide: https://huggingface.co/docs/hub/datasets-cards
{{ card_data }}
---

# Dataset Card for {{ pretty_name | default("Dataset Name", true) }}

<!-- Provide a quick summary of the dataset. -->

{{ dataset_summary | default("", true) }}

## Dataset Details
This dataset is designed for **Amharic idiom classification** using multilingual transformer models. It supports a three-class classification task that distinguishes between:

- **Idiom**: Expressions whose meaning cannot be directly inferred from the literal meaning of their individual words.
- **Proverb**: Traditional Amharic sayings that convey general wisdom, advice, or cultural knowledge.
- **Literal**: Expressions whose meanings are interpreted directly from their surface form without figurative interpretation.

The dataset aims to support research in low-resource natural language processing, particularly figurative language understanding, multilingual representation learning, and computational processing of Amharic.

## Dataset Statistics

| Category | Number of Samples |
|---|---:|
| Idiom | 2,390 |
| Literal | 2,390 |
| Proverb | 1,444 |
| **Total** | **6,224** |

*(Update these values if releasing the complete 6,224-expression version.)*

## Dataset Structure

Each instance contains the following fields:

| Field | Description |
|---|---|
| `text` | Amharic expression used as model input |
| `label` | Class label (Idiom, Proverb, Literal) |
| `label_id` | Numerical label encoding |


Example:

```json
{
  "text": "አፉን ይዞ ተቀመጠ",
  "label": "Idiom",
  "label_id": 0
}
The dataset consists of manually annotated Amharic expressions collected from linguistic resources, educational materials, literary sources, and publicly available text resources. Each expression was categorized according to predefined annotation guidelines based on its semantic interpretation and usage. The dataset is intended for evaluating machine learning and deep learning models for Amharic figurative expression classification.

- **Curated by:** Anduamlak Abebe Fenta and Melkam Enyew Gashaw
- **Funded by:** No external funding was received for the development of this dataset.
- **Shared by:** Anduamlak Abebe Fenta and Melkam Enyew Gashaw
- **Language(s) (NLP):** Amharic (አማርኛ)
- **License:** Dataset annotations and derived metadata are released under CC BY 4.0. Original source materials remain subject to their respective copyright restrictions.

### Dataset Sources [optional]

<!-- Provide the basic links for the dataset. -->

- **Repository:** Hugging Face Datasets Hub (URL will be added after publication)
- **Paper [optional]:** *Amharic Idiom Classification Using Multilingual Transformer Models* (associated research publication)
- **Demo [optional]:** Not available

## Uses

<!-- Address questions around how the dataset is intended to be used. -->

### Direct Use

This dataset is intended for research and development in **Amharic figurative language processing** and **low-resource natural language processing (NLP)**. It can be directly used for:

- Three-class classification of Amharic expressions into **Idiom**, **Proverb**, and **Literal** categories.
- Training and evaluating machine learning, deep learning, and transformer-based language models.
- Benchmarking multilingual and African-language-focused pretrained language models.
- Studying figurative language understanding in morphologically rich and low-resource languages.
- Developing explainable AI (XAI) methods for Amharic NLP classification tasks.

The dataset is designed primarily for academic research and evaluation purposes. Users should consider the cultural and linguistic context of Amharic expressions when applying the dataset to downstream tasks.

### Out-of-Scope Use

This dataset is not intended for applications requiring general-purpose language understanding, real-time decision-making, or automated interpretation of sensitive cultural content without human validation. It should not be used for:

- Generating or evaluating offensive, harmful, or discriminatory content.
- Making decisions about individuals or groups.
- Replacing expert linguistic interpretation in cultural, educational, or legal contexts.
- Assuming complete coverage of Amharic idiomatic and proverbial expressions.

The dataset focuses specifically on isolated Amharic expressions and their classification into Idiom, Proverb, and Literal categories. It may not perform well for tasks requiring contextual figurative language understanding, dialogue interpretation, or broader semantic reasoning.

## Dataset Structure

The dataset is organized as a supervised three-class classification dataset. Each instance contains an Amharic expression and its corresponding category label.


The dataset is divided using a stratified split to preserve class distribution:

- Training set: 80%
- Validation set: 10%
- Test set: 10%

Fixed split identifiers are maintained to support reproducible evaluation.

## Dataset Creation

### Curation Rationale

This dataset was created to address the lack of publicly available benchmarks for Amharic figurative language understanding. Existing NLP resources for Amharic mainly focus on tasks such as sentiment analysis, named entity recognition, and text classification, while figurative language processing remains underexplored.

The dataset provides a benchmark for evaluating multilingual transformer models and traditional deep learning approaches on a challenging low-resource language task involving semantic interpretation and cultural knowledge.

### Source Data

The dataset was collected from multiple Amharic linguistic and cultural resources, including:

- Amharic idiom and proverb collections.
- Educational materials and textbooks.
- Publicly available textual sources.

The collected expressions were manually reviewed and annotated according to predefined linguistic guidelines. Each expression was categorized based on whether its meaning represented a figurative expression (Idiom), a traditional saying (Proverb), or a direct/literal interpretation (Literal).


#### Data Collection and Processing

<!-- This section describes the data collection and processing process such as data selection criteria, filtering and normalization methods, tools and libraries used, etc. -->

{{ data_collection_and_processing_section | default("[More Information Needed]", true)}}

#### Who are the source data producers?

<!-- This section describes the people or systems who originally created the data. It should also include self-reported demographic or identity information for the source data creators if this information is available. -->

{{ source_data_producers_section | default("[More Information Needed]", true)}}

### Annotations [optional]

<!-- If the dataset contains annotations which are not part of the initial data collection, use this section to describe them. -->

#### Annotation process

<!-- This section describes the annotation process such as annotation tools used in the process, the amount of data annotated, annotation guidelines provided to the annotators, interannotator statistics, annotation validation, etc. -->

{{ annotation_process_section | default("[More Information Needed]", true)}}

#### Who are the annotators?

<!-- This section describes the people or systems who created the annotations. -->

{{ who_are_annotators_section | default("[More Information Needed]", true)}}

#### Personal and Sensitive Information

<!-- State whether the dataset contains data that might be considered personal, sensitive, or private (e.g., data that reveals addresses, uniquely identifiable names or aliases, racial or ethnic origins, sexual orientations, religious beliefs, political opinions, financial or health data, etc.). If efforts were made to anonymize the data, describe the anonymization process. -->

{{ personal_and_sensitive_information | default("[More Information Needed]", true)}}

## Bias, Risks, and Limitations

<!-- This section is meant to convey both technical and sociotechnical limitations. -->

{{ bias_risks_limitations | default("[More Information Needed]", true)}}

### Recommendations

<!-- This section is meant to convey recommendations with respect to the bias, risk, and technical limitations. -->

{{ bias_recommendations | default("Users should be made aware of the risks, biases and limitations of the dataset. More information needed for further recommendations.", true)}}

## Citation [optional]

<!-- If there is a paper or blog post introducing the dataset, the APA and Bibtex information for that should go in this section. -->

**BibTeX:**

{{ citation_bibtex | default("[More Information Needed]", true)}}

**APA:**

{{ citation_apa | default("[More Information Needed]", true)}}

## Glossary [optional]

<!-- If relevant, include terms and calculations in this section that can help readers understand the dataset or dataset card. -->

{{ glossary | default("[More Information Needed]", true)}}

## More Information [optional]

{{ more_information | default("[More Information Needed]", true)}}

## Dataset Card Authors [optional]

{{ dataset_card_authors | default("[More Information Needed]", true)}}

## Dataset Card Contact

{{ dataset_card_contact | default("[More Information Needed]", true)}}
