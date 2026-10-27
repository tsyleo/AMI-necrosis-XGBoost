# AMI intestinal necrosis model

Release package: **v1.0.0**; prepared **2026-10-27**.

This repository supports citation of the associated article and access to research materials.

## Public files

| File | Purpose |
|---|---|
| `encrypted/AMI_code_model_v1.0.0_20261027.7z` | Encrypted code and fixed-model package |
| `SHA256SUMS.txt` | Release-file integrity checks |
| [ACCESS_REQUEST.md](ACCESS_REQUEST.md) | How to request access |
| [TERMS_OF_ACCESS.md](TERMS_OF_ACCESS.md) | Access and use conditions |
| [docs/MODEL_CARD.md](docs/MODEL_CARD.md) | Model, inputs, reported results and limitations |
| [docs/DATA_AVAILABILITY.md](docs/DATA_AVAILABILITY.md) | Data scope and reproducibility boundary |

The encrypted archive contains analysis and prediction code, ten fixed XGBoost models, input documentation, synthetic tests, aggregate study results and research application source code. It excludes real patient records, production databases, account credentials and deployment secrets. Downloading the encrypted archive does not provide a decryption password or permission to use its contents.

## Fixed model and reported results

The model uses 18 pre-coded predictors and takes the arithmetic mean of the probabilities from ten XGBoost models to estimate intestinal necrosis confirmed during the index admission. The fixed classification threshold is **0.57**. Classification uses the unrounded probability; a probability exactly equal to 0.57 is assigned to the high-risk group.

Under the hospital-based split confirmed by the study team, centre 1 supplied the development set (**n=230**), and centres 2–3 supplied the external validation set (**n=98**). The reported study results were a development 10-fold OOF AUROC of **0.827 (95% CI 0.770–0.883)** and an external-validation AUROC of **0.826 (95% CI 0.742–0.910)**.

The clinical input mapping was confirmed by the study team on 2026-10-26.

## Access and use

Follow the [access instructions](ACCESS_REQUEST.md) and contact the corresponding author, **Lie Yang**, at **lie_222@163.com**. Requests are reviewed according to their intended purpose; no fixed review deadline or automatic password delivery is promised.

After approval, verify the files against `SHA256SUMS.txt`, decrypt the archive locally using credentials supplied through a separate channel, and follow the instructions inside the package. Do not publish decryption credentials, decrypted controlled-access materials or patient records.

## Citation and use boundary

Please cite the associated article and the release version used. `CITATION.cff.template` remains a template; complete the author details, repository URL and article information before renaming it to `CITATION.cff`.

This package is for research evaluation. It does not establish clinical effectiveness and must not independently determine diagnosis, revascularization, surgery or other treatment. Patient-level data are not publicly distributed. Synthetic examples test software behavior and cannot reproduce the article's performance estimates. See the model card, data availability statement and access terms for further details.

中文说明：[README_zh-CN.md](README_zh-CN.md).
