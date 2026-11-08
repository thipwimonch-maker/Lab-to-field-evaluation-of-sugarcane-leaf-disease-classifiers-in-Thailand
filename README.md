# Sugarcane leaf disease: lab-to-field evaluation — code

Code for the paper *What curated benchmarks miss: leakage auditing, controlled augmentation tests and blinded field evaluation of a deployed sugarcane leaf disease classifier* (submitted to *Computers and Electronics in Agriculture*).

## Contents
- `sugarcane_lab_to_field.ipynb` — training (S1–S6, five architectures), evaluation and all add-on analyses reported in the paper.
- `requirements.txt` — Python packages (versions tested in Google Colab, Python 3.13; the exact versions used during the original experiments were not recorded).

## How to run
1. Open the notebook in Google Colab with a GPU runtime (tested on NVIDIA A100-SXM4-40GB, torch 2.14.1+cu130, CUDA 13.0).
2. Add `KAGGLE_USERNAME` and `KAGGLE_KEY` to Colab Secrets (used to download the public datasets).
3. Edit the paths in the **Config** cell.
4. Run in order: Config → Pre-flight → Cell 0 → 1.x → 3.1 → 4.x → S1–S6 → add-on cells (A0 → A10, B1–B4, S4-fair v2, C1, S2-fixed, A7c, Z).
   Cells already completed are skipped (results are checked on disk), so the notebook can be resumed after a disconnect.
5. Cells preceded by a **Note:** cell are earlier versions kept for transparency; their results are not reported.

## Data
| Dataset | Availability |
|---|---|
| PlantVillage | public (Kaggle) |
| PlantDoc | public (Singh et al., 2020) |
| Sugarcane Leaf Disease dataset | public, Mendeley Data, doi:10.17632/9424skmnrk.1 (Daphal and Koli, 2022) |
| Thai sugarcane leaf dataset | not public — request from its owners (Baipod et al., 2025) |
| LINE field images and expert labels | not shared, to protect user privacy (ethics approval: Human Research Ethics Committee, Mahasarakham University, no. 452-459/2569) |

The C1.x field-evaluation cells need the field images and are skipped when `FIELD_DIR` does not exist.

## Citation
[add the paper citation and the Zenodo DOI after publication]

## License
Code: MIT License (see `LICENSE`). The license covers the code only; it does not apply to the datasets listed above.
