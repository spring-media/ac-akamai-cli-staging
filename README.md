# Akamai CLI: Domain Staging command

This repo is an command for Akamai CLI to staging given domains.

## Install

Installation is done via `akamai install`:

```
$ akamai install https://github.com/spring-media/ac-akamai-cli-staging.git
```

Running this will run the system `python setup.py` automatically. 

## Updating

To update to the latest version:

```
$ akamai update staging
```

## Running

To run it:

```
$ akamai staging hosts www.akamai.com
$ akamai staging hosts www.akamai.com,www.akamai.de
```
