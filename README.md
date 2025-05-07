# GeoNER
This project provides a framework for evaluating Named Entity Recognition (NER) in geoscientific texts using the [Flair NLP library](https://github.com/flairNLP/flair) and domain-specific schemas. It supports user-provided PDF corpora and integrates the OzRock schema, a publicly available geoscience NER schema, for entity tagging.
Users can test the NER performance on their own geoscientific documents (e.g., on lithium, iron, copper, or other mineral systems), using pretrained models and schema-based annotations.

---

## Features

- **Custom Corpus Compatibility**: Use your own PDF files (e.g., on gold, rare earths) for NER evaluation.
- **Integrated OzRock Schema**: Uses the OzRock schema available at [OzROCK](https://github.com/majiga/OzROCK).
- **NER Model Training/Evaluation**: Scripts to train or evaluate a Flair-based SequenceTagger.
- **Visual Evaluation**: Generates confusion matrices and F1 score plots per entity class.
- **Flexible Schema Extension**: Easily adapt or extend to use other geological schemas.

---

## Installation

```bash
git clone https://github.com/SPVillacorta/GeoNER.git
cd GeoNER
pip install -r requirements.txt
```

---

## How to Use

1. **Prepare your Corpus**
   - Place your PDF files in a new folder, e.g., `data/pdf/`

2. **Run the Preprocessing Script**
   - Extract sentences using `pdfplumber`

3. **Train or Evaluate the NER Model**
   - Use the provided script to train the model on OzRock or evaluate NER tagging.

4. **Review the Outputs**
   - Confusion matrix and F1 scores will be generated to assess performance.

> The model has been trained with the OzRock schema. You can adapt the code to use other schemas if needed.

---

## Citation
If you use this repository, code, or dataset in your research, please cite the following publication:

Villacorta, S.P., Lindsay, M., Klump, J., Gessner, K., Gray, E., & McFarlane, H. Assessing Named Entity Recognition by using Geosciences Domain Schemas: The case of Mineral Systems. Frontiers in Earth Science, 13, 1530004. [https://doi.org/10.3389/feart.2025.123456](https://doi.org/10.3389/feart.2025.1530004)

BibTeX
@article{Villacorta2025GeoNER,
  title     = {Assessing Named Entity Recognition by using Geosciences Domain Schemas: The case of Mineral Systems},
  author    = {Villacorta, S.P., Lindsay, M., Klump, J., Gessner, K., Gray, E., & McFarlane, H},
  journal   = {Frontiers in Earth Science},
  year      = {2025},
  volume    = {13},
  pages     = {1--16},
  doi       = {[10.3389/feart.2025.123456](https://doi.org/10.3389/feart.2025.1530004)}
}

And acknowledge:
> Enkhsaikhan, B., et al. (2021). *OzRock: A geoscientific named entity recognition evaluation set.* https://github.com/majiga/OzROCK

---

## License

This repository is licensed under the MIT License.

---

## Contact
Please email your questions or comments to Sandra Villacorta.

---

## Contributing

We welcome pull requests and suggestions for improvement. Please open an issue to discuss your ideas.

---

## Acknowledgments

Thanks to CSIRO and the Geological Survey of Western Australia for supporting research.
