# Installations for Workshop

## Introduction
This workshop will cover an end-to-end, hands-on experience of training a simple LLM using Hugging Face that will then be deployed using a Docker container on a local machine or using GCP. Follow the steps below to continue

## Game Plan
In this workshop, we will do the following:
- Fine-tune a Hugging Face LLM (LLaMa 3 - 8B Instruct) on Colab Free Tier GPUs
- Log our training run using Weights & Biases
- Create a simple web-app using Gradio/StreamLit to host our LLM
- Containerize the web-app using Docker
- Deploy the container on the local machine or on Google Cloud Platform

## Machine Installations

### Docker
To install Docker, follow these steps according to your platform:
- [Linux](https://docs.docker.com/desktop/install/linux-install/)
- [Windows](https://docs.docker.com/desktop/install/windows-install/)
- [MacOS](https://docs.docker.com/desktop/install/mac-install/)

## Package Installations

> :warning: You will need a Hugging Face account to work with this, so please [sign up here](https://huggingface.co/). Also, create an account with Weights & Biases as well for experiment tracking [here](https://wandb.ai).

### tl;dr
Run the following commands
```
python3.10 -m venv .venv

# If using linux or macos
source .venv/bin/activate
# If using Windows
.venv/Scripts/activate

pip3 install datasets accelerate transformers peft wandb bitsandbytes xformers gradio -qq
```

### Longer version

#### 🤗 Transformers
We use Transformers to download and load our models.
```
pip install transformers
```
#### 🤗 PEFT
PEFT stands for Parameter-Efficient Fine-Tuning, which will allow us to fine-tune large models on smaller consumer hardware.
```
pip install peft
```
#### 🤗 Accelerate
Accelerate is a library that will allow us to leverage our GPUs in the most optimized way possible and make it easier for us to configure it.
```
pip install accelerate
```
#### 🤗 Datasets
Datasets will allow us to download and register our datasets in a few simple steps!
```
pip install datasets
```
#### BitsAndBytes
We use BitsAndBytes to perform QLoRA effectively.
```
pip install bitsandbytes
```
#### XFormers
We use XFormers to get efficient attention model implementations and kernels.
```
pip install xformers
```
#### Weights & Biases
We will use WandB for quick experiment tracking. Make sure you create an account with WandB to log your runs correctly.
```
pip install wandb
```
#### Gradio
We use Gradio to create a simple web-app that can act as a front-end for our LLM.
```
pip install gradio
```

## Google Cloud Platform

>:warning: This part is optional. If you wish, you can follow the GCP-specific sections on a local machine too.

> :warning: This step requires billing accounts and may incur charges. Please make sure you destroy all resources when you are done using them. The intended estimated cost of this workshop at best should not exceed USD 5.

If you would like to follow along for the GCP side of the workshop, please make sure you get a Google Cloud Platform account created with an active Billing Account.
To create a Free Tier account (provided you have never made a GCP account before), use [this website](https://cloud.google.com/free) and log in.
Upon logging in, you will notice a blue band on the top of the webpage telling you to register a Credit/Debit card to activate the billing account. Please go ahead and activate the same by entering your details.
