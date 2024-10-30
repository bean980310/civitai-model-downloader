# civitai-downloader
Model Downloader Package and CLI for CivitAI.

It is recommanded on Amazon Web Services, Microsoft Azure, Google Cloud Platform.

## How to Use

First, Install civitai-downloader

```bash
# Install from PyPI
pip3 install civitai-downloader

# Install from GitHub
pip3 install git+https://github.com/bean980310/civitai-downloader.git

# Install from Source
git clone https://github.com/bean980310/civitai-downloader.git
cd civitai-downloader
pip3 install -e .
```

and, Insert your Access token

```python
from civitai_downloader.token.token import prompt_for_civitai_token

prompt_for_civitai_token()
```

Import Your CivitAI API Token and Next, Download a model

```python
from civitai_downloader.token.token import get_token
from civitai_downloader.download.download import download_file, civitai_download

token=get_token()

# example
url_download(url="https://civitai.com/api/download/models/90854", local_dir="./models/checkpoints/sd15", token=token)

# or
civitai_download(model_id=90854, local_dir="./models/checkpoints/sd15", token=token)
```

Also, you can use to civitai-downloader command line

```bash
# example
civitai-downloader-cli download 90854

# prefix local dir
civitai-downloader-cli download 90854 --local-dir ./models/checkpoints/sd15

# to use url
civitai-downloader-cli url-download https://civitai.com/api/download/models/90854
```