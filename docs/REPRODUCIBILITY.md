# Reproduction and preservation

## Preservation

The original source files remain untouched. In the public notebook, only two Hugging Face authentication token literals (zero-based cells 78 and 91) were replaced with `__import__("os").environ["HF_TOKEN"]`. All other source text, Markdown, outputs, execution counts, metadata and notebook formatting are preserved.

Set `HF_TOKEN` in the notebook kernel's environment before running those authentication cells. Use your own Hugging Face token and keep it out of committed files.

`verification/original-sha256.json` records byte-level hashes of the 18 files in the source archive. `verification/public-notebook.json` records the original and public notebook hashes and the scope of the two authorised replacements. Figures in `assets/` were decoded from existing PNG outputs, not recreated.

## Requirements visible in the notebook

- Python 3.11 or newer is needed for the use of `datetime.UTC`.
- Notebook environment: Jupyter or Google Colab.
- Scientific stack: NumPy, pandas, scikit-learn, matplotlib, seaborn.
- NLP stack: zstandard, fasttext, sentence-transformers, transformers, torch, huggingface_hub, accelerate, bitsandbytes and SentencePiece where required by the selected models.
- A compatible GPU/software environment for the original 4-bit quantisation calls.
- Access to any gated Hugging Face models under their own conditions.

No exact environment lock was supplied. Installing current package versions is not a guarantee that the historical notebook will run unchanged. No new dependency lock or successful full-run claim is made.

## External assets and paths

The source archive contains filtered/derived JSONs, train/test JSONs and the notebook, but no `.zst` dumps or `cc.en.300.bin`. Initial extraction requires the course-provided dumps; fastText sections require the model file. Model downloads/training can be expensive in time and memory.

Several cells reference `./drive/MyDrive/PLNE_EnriqueVicente_JoseMontesinos/`; some later cells use filenames relative to the working directory. To preserve the original code, reproduce its expected directory layout in your own workspace and provide input files at both required locations rather than editing this preserved notebook.

The random summarisation examples were selected without a fixed seed, and the notebook explicitly asks reviewers not to rerun the example-selection cell if they want to retain the same examples. Read the saved outputs first. A future reproducible experiment should be a separate version with a fixed environment, input hashes, seeds and a development split.
