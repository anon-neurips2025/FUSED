# FUSED: An Integrative Foundation Model Approach for Drug
Response Prediction

FUSED is a deep learning framework for predicting drug response in cancer cell lines using multi-omics data and foundation model based drug embeddings, but excels in only-transcriptomic settings. This repository contains code, data, and scripts for reproducing the experiments in our NeurIPS 2025 submission. For anonymity reasons, this repo was created using only web ui, hence the src folder is a zip that needs to be unpacked locally.

## Project Structure

- `src/`
  - `data/`  
    Raw and processed datasets, drug embeddings, and omics features.
  - `FUSED/`  
    Main PyTorch models, training scripts, and utilities for our attention-based fusion architecture.
  - `prog/`  
    Keras/TensorFlow models for FM Integration, experiment scripts, and analysis notebooks.
  - `pytorch_src/`  
    Alternative PyTorch implementations and scripts.

## Getting Started

1. **Download zip folder**

2. **Install dependencies**
   - PyTorch: See `src/FUSED/requirements.txt`
   - TensorFlow/Keras: See `src/prog/environment.yml`
   - Other requirements: See respective `requirements.txt` files.

3. **Prepare data**
   - Download and extract datasets into `src/data/`.
   - Ensure drug embeddings are present in `src/data/drug_embeddings/`.
   - scripts to recreate embeddings are present in `src/prog/`

4. **Run experiments**
   - PyTorch (attention fusion):  
     ```sh
     cd src/FUSED
     bash run_attn.sh
     ```
   - Keras (DeepCDR):  
     ```sh
     cd src/prog
     python run_DeepCDR.py
     ```

5. **Evaluation**
   - Use Jupyter notebooks in [`src/prog`](src/prog) for analysis and plotting.

## Citation

If you use FUSED in your research, please cite our paper.

## License

See [`LICENSE`](LICENSE).

## Contact

For questions, please contact the authors or open an issue.
