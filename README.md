# Zenpy Incidents Report

Sample script for Zendesk Administrators utilising Zendesk API client for Python [Zenpy](https://github.com/facetoe/zenpy) to create CSV report of number of incidents per problem ticket. Credentials can be configured in .env file or
overriden through optional arguments.

## Getting started

- Clone repository
- Go to repository directory
- Install requirments `python3 -m pip install -r requirments.txt`
- [Optional] Create .env file using your favourite text editor to store your credentials

### .env file example

SUBDOMAIN=subdomain_only \
USERNAME=admin@example.com \
APITOKEN=foobarbaz

## Usage

`python3 script.py [-h] [-s SUBDOMAIN] [-o OAUTHTOKEN] [-u USERNAME] [-p PASSWORD] [-t APITOKEN] [--start STARTDATE] [--end ENDDATE]`

options: \
-h, --help show this help message and exit \
-s SUBDOMAIN Zendesk Subdomain (e.g. d3v-test) \
-o OAUTHTOKEN Pre-generated OAuth2 token with "tickets:read write" scope \
-u USERNAME Agent Zendesk email address \
-p PASSWORD Agent Zendesk password \
-t APITOKEN \
--start STARTDATE Lower limit of incident ticket creation date (YYYY-MM-DD). Defaults to last week. \
--end ENDDATE Upper limit of incident ticket creation date (YYYY-MM-DD). Defaults to today
