# Evidence Uploader Backend

A Flask (Python) app for uploading dispute evidence links to the blockchain. Files may be provided via external link, or uploaded directly to the
hosted [backend](../backend/README.md). Metamask is used for executing the transaction.

A [URL Shortener](https://github.com/solomondefi/link-shortener) is used to shorten links to reduce blockchain gas fees.

**TBD - Include backend implementation**

## Setup
These instructions have been tested on Ubuntu 20.04, but should translate well to OSX.

### Install/update `poetry`

#### Ubuntu:

It may be necessary to install a newer version of Python, e.g.

```
sudo add-apt-repository ppa:deadsnakes/ppa
sudo apt install python3.9-dev
```


```
sudo apt update
sudo apt install python3-pip
pip3 install poetry
```

#### OSX (untested)

```
brew install poetry pyenv
pyenv install 3.9.4
pyenv local 3.9.4
```

### Install python packages

```
poetry install
```

## App configuration table

Key                          | Default            | Description
---------------------------- | ------------------- | ---------------------
MAX_FILE_TTL                 | 90                  | Maximum lifetime of evidence files in days
APP_DOMAIN                   | evidence-api.localdev.com | Name of the server, must match production server name.
APP_PORT                     | 5000                |
S3_BUCKET                    | evidence-uploads    | S3 bucket for App files
S3_ENDPOINT                  |                     | S3 endpoint
S3_KEY                       |                     | S3 client key
S3_SECRET                    |                     | S3 client secret
S3_REGION                    |                     | S3 region
SHORTENER_URL                |                     | Private URL shortener for project links
SHORTENER_ACCESS_TOKEN       |                     | Access token for URL shortener