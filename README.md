# Akamai CLI: Domain Staging command

This repo is an command for Akamai CLI to staging given domains and to make it easy to handle sandbox with pipelines.

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

## Running to staging domain 

To run it:

```
$ akamai staging hosts www.akamai.com
$ akamai staging hosts www.akamai.com,www.akamai.de
```

## create a sandbox for a given pipeline 

To create and run a sandbox for given domain and pipeline. The default pipeline environment is "stage":

```
akamai staging sandbox_start --pipeline www.autobild.de --pipeline-dir=<local_dir_of_pipeline>
```

## renew a running sandbox with the changes of the pipeline 

```
akamai staging sandbox_renew --pipeline www.autobild.de
```

## stop and destroy a running sandbox

```
akamai staging sandbox_stop --pipeline www.autobild.de
```
