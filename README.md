# About

This module contains the basic cloud implementations of Textalytics (https://textalytics.io) core capabilities.

Textalytics build and delivers custom NLP models for NER and entity-resolution for different domains. 
Further Textalytics caters to the needs of organizations that have a need to deploy these models in an air-gappend 
environemnt where no data can go out of internal network. 

The open source version of Textalytics will implement adapters for the interfaces to popular Cloud NLP APIs (GCP, AWS, Azure).
It will also provide the API implementation to enable self-hosting on cloud or on-prem.

# PyPi package

This module is availabe in pypi

Usage:

`pip install textalytics-cloud-api-adapters`

# Local development

You will need Python 3.9+ installed. This project uses `poetry` to manage dependencies.

`poetry` can be installed with `brew` on a Mac.

* Get latest code from github
* Create a virtual environment

`python -m venv venv`

* Initialize poetry and install dependencies

`poetry init`

`poetry install`

* At this point you will be able to build

`poetry build`

* Tests can be run with 

`poetry run test`

# GCP

Follow along instructions to get setup with being able to invoke APIs in GCP
* https://github.com/googleapis/python-language

## Authentication

Following above instructions will result in credentials being stored in a local directory. On a Mac the `default` 
credentials will be saved in `~/.config/gcloud/application_default_credentials.json`

## Python Client Library

`poetry add google-cloud-language`

# AWS

* Download aws cli tools for your system
* Setup API keys via AWS console  
* Run `aws configure` and add the API keys to the local configuration

On a mac the above stores the credential in `~/.aws/credentials` file. The default namespace will be named `default`.

## Auth requirements

In its current implementation, the implementation expects `aws_access_key_id` and `aws_secret_access_key` 
to be availble in the `default` namespace.

## Python Client Library

`poetry add boto3`

# Azure

Follow instructions from here:
* https://docs.microsoft.com/en-us/azure/cognitive-services/text-analytics/quickstarts/client-libraries-rest-api
* https://pypi.org/project/azure-ai-textanalytics/5.1.0/

## Auth requirements

In its current implementation, the implementation expects `AZURE_TEXT_ANALYTICS_ENDPOINT` and `AZURE_TEXT_ANALYTICS_KEY`
to be available as environment variables.

## Python Client Library

`poetry add azure-ai-textanalytics`

# Textalytics Hosted

Follow instructions from here:
* https://textalytics.io/doc
* https://pypi.org/project/textalytics-python-client/

## Auth requirements

Follow instructions above. The implementation expects the following to be available as environment variables:
* `TEXTALYTICS_ENDPOINT` - Textalytics hosted url
* `TEXTALYTICS_USERNAME` - Textalytics hosted username 
* `TEXTALYTICS_PASSWORD` - Textalytics hoted password

Refer to example:
https://github.com/Textalytics/textalytics-python-client/blob/main/tests/test_text_analysis.py

## Python Client Library

`poetry add textalytics-python-client`

