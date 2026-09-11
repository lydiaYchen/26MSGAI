# MSGAI lab instructions

## Course overview

This course covers the fundamentals and applications of generative AI. The labs combine hands-on exercises with TA-led discussion and prepare you for the quizzes and group project. See the [course page](../README.md) for the current schedule and assessment requirements.

The notebooks currently available are:

- Part 1: [Diffusion, VAE, and flow matching](#part-1-diffusion-vae-and-flow-matching)
  - [Lab 1: Diffusion models](Lab%20%231/lab_diffusion_1.ipynb) — DDPM forward process, noise-prediction loss, pretrained sampling, and DDIM.
  - [Lab 2: VAE and latent diffusion](Lab%20%232/lab_vae_diffusion_2.ipynb) — AE vs VAE on MNIST, pretrained VAE reconstruction, latent diffusion, and two-dimensional flow matching.
- Part 2: [Large language models](#part-2-large-language-models)
  - [Lab 3: LLMs, Transformers, and SFT](Lab%20%233/Lab_LLM_transformer_3.ipynb) — generation, chat templates, output probabilities, representations, attention, and supervised fine-tuning.

Later lab topics follow the course schedule; their notebooks will be added separately.

## Prerequisites

Set up your environment before attending the lab so that session time can focus on the exercises. You need a computer capable of loading the models, an internet connection for the initial downloads, and enough disk space for datasets and model weights.

Alternatively, use [Google Colab](https://colab.google.com) or another GPU notebook environment. Upload the complete `Labs` folder so that relative paths and supporting files remain available, and install the supplied requirements in that environment.

### Technical requirements

The experiments use **Python 3.11** and **PyTorch**. Create a separate virtual environment using the supplied [requirements.txt](requirements.txt). From the `26MSGAI` directory, run:

```bash
python -m venv .venv
source .venv/bin/activate
python -m pip install --upgrade pip
python -m pip install -r Labs/requirements.txt
python -m ipykernel install --user --name msgai26 --display-name "MSGAI26"
jupyter lab Labs
```

On Windows, replace the activation command with `.venv\Scripts\activate` in Command Prompt or `.\.venv\Scripts\Activate.ps1` in PowerShell. Select the **MSGAI26** kernel in Jupyter.

A CUDA GPU is recommended for pretrained diffusion models and Gemma, especially the SFT exercise. The smaller AE/VAE and flow-matching exercises can run on CPU. If you need a different PyTorch build for your GPU, consult the [official installation instructions](https://pytorch.org/get-started/locally/) and the [version-specific commands](https://pytorch.org/get-started/previous-versions/) for the versions pinned in `requirements.txt`.

Check GPU access from your notebook:

```python
import torch
print("PyTorch:", torch.__version__)
print("CUDA available:", torch.cuda.is_available())
if torch.cuda.is_available():
    print("GPU:", torch.cuda.get_device_name(0))
```

Run each notebook from top to bottom, with its working directory set to its `Lab #N` folder. Restart the kernel when changing labs to release model memory. Datasets are downloaded to `Labs/data`; pretrained models use the Hugging Face cache.

## Part 1: Diffusion, VAE, and flow matching

Run the setup and model-loading cells before the session to download the required models and datasets. Work through the numbered exercises, change the requested parameters, and record your observations in Markdown cells.

Lab 1 explores diffusion training and sampling. Lab 2 compares autoencoders and variational autoencoders, examines pretrained latent diffusion, and includes a short flow-matching training experiment. Follow the latent-dimension and random-seed instructions when comparing results.

## Part 2: Large language models

Before attending the lab, run the authentication and model-loading cells: model access and downloads may take time.

Lab 3 uses **Gemma-2-2b-it**. Complete the indicated `user_inputs` and attention-code placeholders, then compare the model's outputs and internal representations. The final exercise demonstrates one SFT update with LoRA, followed by 20 updates and a before-and-after comparison on held-out prompts. Its setup cell installs the additional `peft` dependency.

### Hugging Face credentials and pre-downloading models

1. Create a Hugging Face account and accept the access terms on the [Gemma-2-2b-it model page](https://huggingface.co/google/gemma-2-2b-it). Confirm that the account has access before downloading the model.
2. Create a [read token](https://huggingface.co/docs/hub/security-tokens) for that account.
3. Copy `Labs/.env.template` to `Labs/.env` and fill in `HUGGINGFACE_API_KEY`.
4. Run the notebook's authentication and model-loading cells. The notebooks call `load_dotenv()` to read the token. In a hosted notebook environment, you can instead set `HUGGINGFACE_API_KEY` as an environment variable.

Do not hardcode tokens in notebooks or commit your `.env` file. The supplied `Labs/.gitignore` excludes `.env`.

The lab also downloads an MS MARCO relevance scorer. Its score measures question–answer relevance; it does not verify factual correctness.

## Working on the exercises and submitting work

The labs are ungraded, but their content is included in the quizzes. Keep your code, plots, generated outputs, and written observations in your working notebooks for discussion and revision. The course page specifies the current quiz and group-project requirements; submit required project materials through ILIAS.

We recommend using Git to track your changes. The distributed notebooks have no outputs. If you use an output-stripping hook for Git, retain an executed copy with outputs whenever a submission requires a notebook.
