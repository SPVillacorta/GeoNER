# GeoNER-SchemaEval
This project provides a framework for evaluating Named Entity Recognition (NER) in geoscientific texts using the [Flair NLP library](https://github.com/flairNLP/flair) and domain-specific schemas. It supports user-provided PDF corpora and integrates the [OzROCK](https://github.com/majiga/OzROCK) schema, for entity tagging.
Users can test the NER performance on their own geoscientific documents related to mineral systems, using pretrained models and schema-based annotations.

---

## Features

- **Custom Corpus Compatibility**: Use your own PDF files on mineral systems (e.g., on gold, rare earths) for NER evaluation.
- **Demonstration of the use of a geoschema**: Uses the [OzROCK](https://github.com/majiga/OzROCK) schema.
- **NER Model Training/Evaluation**: Scripts to train or evaluate a Flair-based SequenceTagger.
- **Visual Evaluation**: Generates confusion matrices and F1 score plots per entity class.
- **Flexible Schema Extension**: Easily adapt or extend to other geological schemas.

---

## Try on Google Colab
Run GeoNER directly in your browser by clicking 
[![Abrir en Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/SPVillacorta/GeoNER-SchemaEval/blob/main/notebooks/geoner_schema_eval.ipynb)
The notebook includes:
Installation of required dependencies (Flair, pdfplumber, etc.).
Example usage of the pretrained NER model based on the OzRock schema.
Entity recognition and basic evaluation on sample texts.
Visual outputs such as confusion matrices and class-wise F1 scores.

📁 Note: You can upload your own corpus on mineral systems (e.g., papers on lithium, iron, or copper) directly to the Colab session and process them by updating the PDF file in the notebook.

...

## Installation (Running Locally)

If you prefer to run this project on your local machine, ensure you have Git and Python (preferably with `conda` or `venv`) installed.

1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/SPVillacorta/GeoNER-SchemaEval.git](https://github.com/SPVillacorta/GeoNER-SchemaEval.git)
    cd GeoNER-SchemaEval
    ```

2.  **Install dependencies:**
    It is recommended to create a virtual environment to manage dependencies:
    ```bash
    python -m venv venv
    source venv/bin/activate  # On Windows: venv\Scripts\activate
    pip install -r requirements.txt
    ```

3.  **Download the pre-trained model:**
    The `best-model.pt` file is approximately 238 MB and is not stored directly on GitHub. You will need to download it manually and place it in the correct directory.
    * **Download Link:** [**Click here to download `best-model.pt` from Google Drive**](YOUR_GOOGLE_DRIVE_DIRECT_DOWNLOAD_LINK_HERE)
        * **Important:** Ensure this Google Drive link is set to "Anyone with the link" for public access.
    * **Placement:** After downloading, place the `best-model.pt` file into the `ozrock/model/` directory within your cloned repository:
        ```
        GeoNER-SchemaEval/
        └── ozrock/
            └── model/
                └── best-model.pt  <-- Place the downloaded file here
        ```

4.  **Run the Jupyter Notebook:**
    Once the model is downloaded and placed, you can run the notebook:
    ```bash
    jupyter notebook notebooks/ner_model_evaluation.ipynb
    ```

```


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

### Example Use Case: Iron Ore Corpus Analysis
This pipeline was originally tested on a collection of 20 PDF research papers related to iron ore deposits in Western Australia. These papers were used to evaluate the performance of NER tagging based on the OzRock schema.

Note: Some of the PDFs used in our experiments were obtained via institutional access or direct purchase. To support reproducibility, we recommend using freely accessible research papers available from sources like Google Scholar. Once downloaded, place your PDF files in the appropriate folder (e.g., data/pdf/) and follow the steps in the How to Use section to extract and process the documents.

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

This repository is licensed under the MIT [LICENSE](LICENSE).

---

## Contact
Please email your questions or comments to Sandra Villacorta.

---

## Contributing

We welcome pull requests and suggestions for improvement. Please open an issue to discuss your ideas.

---

## Acknowledgments

Thanks to CSIRO and the Geological Survey of Western Australia for supporting research.
