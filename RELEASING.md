# Publishing this repository and minting a Zenodo DOI

## 1. Create the GitHub repository
1. Sign in to GitHub as `GArulDalton` and create a new **public** repository named `EdgeLight-GAN` (leave it empty: no README, .gitignore, or license).
2. In this folder run:

```bash
git init -b main
git add .
git commit -m "Initial release of EdgeLight-GAN"
git remote add origin https://github.com/GArulDalton/EdgeLight-GAN.git
git push -u origin main
```

The GitHub link is `https://github.com/GArulDalton/EdgeLight-GAN`.

## 2. Mint the Zenodo DOI
1. Sign in at https://zenodo.org with GitHub, open https://zenodo.org/account/settings/github/ and switch **ON** the toggle for `GArulDalton/EdgeLight-GAN`.
2. On GitHub, open **Releases > Draft a new release**, create the tag `v1.0.0`, title it `EdgeLight-GAN v1.0.0`, and publish.
3. Zenodo archives the release automatically (a minute or two). It reads `.zenodo.json` and `CITATION.cff` for the metadata.
4. Copy the DOI from the Zenodo record. Use the **concept DOI** ("Cite all versions") if you want a link that always points to the latest version, or the version DOI for this exact release.
5. Replace `ZENODO_DOI_PLACEHOLDER` in `README.md` with the DOI, commit, and push. (Do not move the `v1.0.0` tag; later edits do not change the archived release.)

## 3. Before you release
- The code is a reimplementation from the paper description. Put the loss-weight values and any hyperparameters actually used in `configs/default.yaml`, and say in the README whether this is the exact code behind the reported numbers.
- Do not commit datasets or checkpoints larger than 100 MB.
