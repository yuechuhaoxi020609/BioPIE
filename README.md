
# BioPIE Dataset
[![CC BY-NC 4.0][cc-by-nc-shield]][cc-by-nc]

This repository contains the **BioPIE** dataset, as presented in the paper "[BioPIE: A Biomedical Protocol Information Extraction Dataset for High-Reasoning-Complexity Experiment Question Answer](https://arxiv.org/abs/2601.04524v1)". 

## Protocol

The **Protocols** folder contains the cleaned biomedical experiment protocols. These protocols have been preprocessed and are ready for use in research and experimentation.

## IE

The **IE** (Information Extraction) folder contains the BioPIE dataset. Each document in the dataset follows the structure below:

```json
{
  # document ID
  "doc_key": "CNN_ENG_20030306_083604.6",

  # sentences in the document, each sentence is a list of tokens
  "sentences": [
    [...],
    [...],
    ["Pass", "samples", "through", "two", "successive", ...],
    ...
  ],

  # entities (boundaries and entity type) in each sentence
  "ner": [
    [...],
    [...],
    [[[0, 0, "verb"], [1, 1, "cell"], [5, 5, "time"], ...], 
    ...,
  ],

  # relations (two spans and relation type) in each sentence
  "relations": [
    [...],
    [...],
    [[1, 1, 0, 0, "is_object_of"], [0, 0, 8, 8, "use_reagent"], ...],
    ...
  ]
}
````

The entities in the dataset belong to the following classes:
        "verb", "part", "container", "force", "device", "method", "chemical", 
        "concentration", "consumable", "state", "volume", "temperature", "time", 
        "process", "times", "cell", "nucleic acid", "biomaterial", "software", 
        "number", "energy", "speed", "mass", "environment", "length", "data", 
        "organ", "animal", "protein", "polymer", "position", "size", "plant", "blend".

The relations between entities are represented by the following types:
        "is_object_of", "contain", "use_method", "use_device", "use_reagent", 
        "have_property", "apply_material", "is_goal_of", "for_each", "next_step", 
        "to", "or", "have_parameter", "repetitions", "use_software", "from", 
        "in_condition_of", "not", "during", "equal", "based_on".

## QA Dataset

The **QA** folder contains the biomedical experiment question-answering data.

## License

This work is licensed under a
[Creative Commons Attribution-NonCommercial 4.0 International License][cc-by-nc].

## Citation

If you use this dataset in your research, please cite the following paper:

```
@misc{hou2026biopiebiomedicalprotocolinformation,
      title={BioPIE: A Biomedical Protocol Information Extraction Dataset for High-Reasoning-Complexity Experiment Question Answer}, 
      author={Haofei Hou and Shunyi Zhao and Fanxu Meng and Kairui Yang and Lecheng Ruan and Qining Wang},
      year={2026},
      eprint={2601.04524},
      archivePrefix={arXiv},
      primaryClass={cs.AI},
      url={https://arxiv.org/abs/2601.04524}, 
}
```

[cc-by-nc]: https://creativecommons.org/licenses/by-nc/4.0/
[cc-by-nc-image]: https://licensebuttons.net/l/by-nc/4.0/88x31.png
[cc-by-nc-shield]: https://img.shields.io/badge/License-CC%20BY--NC%204.0-lightgrey.svg