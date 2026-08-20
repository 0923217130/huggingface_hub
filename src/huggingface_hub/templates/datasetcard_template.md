---
# For reference on dataset card metadata, see the spec: https://github.com/huggingface/hub-docs/blob/main/datasetcard.md?plain=1
# Doc / guide: https://huggingface.co/docs/hub/datasets-cards
{{ card_data }}
---

# Amharic Idiom Classification Using Multilingual Transformer Models


<!-- Provide a quick summary of the dataset. -->

{{ dataset_summary | default("", true) }}

## Dataset Details

## Dataset Description

This dataset is designed for **Amharic figurative expression classification** using multilingual transformer models. It supports a three-class classification task that distinguishes between:

- **Idiom**: Expressions whose meaning cannot be directly inferred from the literal meaning of their individual words.
- **Proverb**: Traditional Amharic sayings that convey general wisdom, advice, or cultural knowledge.
- **Literal**: Expressions whose meanings are interpreted directly from their surface form without figurative interpretation.

The dataset aims to support research in low-resource natural language processing, particularly figurative language understanding, multilingual representation learning, and computational processing of Amharic.

## Dataset Statistics

| Category | Number of Samples |
|---|---:|
| Idiom | 1,148 |
| Literal | 1,099 |
| Proverb | 694 |
| **Total** | **2,941** |

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
### Dataset Description

This dataset contains Amharic figurative expression samples designed for three-class classification: **Idiom**, **Proverb**, and **Literal**. The dataset was developed to support research on low-resource natural language processing, particularly figurative language understanding using multilingual transformer models.

The dataset consists of manually annotated Amharic expressions collected from linguistic resources, educational materials, literary sources, and publicly available text resources. Each expression was categorized according to predefined annotation guidelines based on its semantic interpretation and usage. The dataset is intended for evaluating machine learning and deep learning models for Amharic figurative expression classification.

- **Curated by:** Anduamlak Abebe Fenta and Melkam Enyew Gashaw
- **Funded by:** No external funding was received for the development of this dataset.
- **Shared by:** Anduamlak Abebe Fenta and Melkam Enyew Gashaw
- **Language(s) (NLP):** Amharic (አማርኛ)
- **License:** Dataset and derived metadata are released under CC BY 4.0. Original source materials remain subject to their respective copyright restrictions.
### Dataset Sources [optional]

<!-- Provide the basic links for the dataset. -->

- **Repository:** {{ repo | default("[More Information Needed]", true)}}
- **Paper [optional]:** {{ paper | default("[More Information Needed]", true)}}
- **Demo [optional]:** {{ demo | default("[More Information Needed]", true)}}

## Uses

<!-- Address questions around how the dataset is intended to be used. -->

### Direct Use

<!-- This section describes suitable use cases for the dataset. -->

{{ direct_use | default("[More Information Needed]", true)}}

### Out-of-Scope Use

<!-- This section addresses misuse, malicious use, and uses that the dataset will not work well for. -->

{{ out_of_scope_use | default("[More Information Needed]", true)}}

## Dataset Structure

<!-- This section provides a description of the dataset fields, and additional information about the dataset structure such as criteria used to create the splits, relationships between data points, etc. -->

{{ dataset_structure | default("[More Information Needed]", true)}}

## Dataset Creation

### Curation Rationale

<!-- Motivation for the creation of this dataset. -->

{{ curation_rationale_section | default("[More Information Needed]", true)}}

### Source Data

<!-- This section describes the source data (e.g. news text and headlines, social media posts, translated sentences, ...). -->

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
