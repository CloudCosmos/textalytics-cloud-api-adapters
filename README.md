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

# AWS


# Azure
