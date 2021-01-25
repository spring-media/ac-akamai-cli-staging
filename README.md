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

## create a sandbox for a defined local pipeline or a property from Akamai 

To create and run a sandbox for a defined domain and pipeline. The default pipeline environment is "stage":
```
akamai staging sandbox_start --type pipeline --pipeline www.autobild.de --pipeline-dir <local_dir_of_pipeline>
```

To create and run a sandbox for a property from Akamai
```
akamai staging sandbox_start --type property --property www.stage.autobild.de_ion --property-domain www.stage.autobild.de
```

## renew a running sandbox

Renew a sandbox based on pipeline
```
akamai staging sandbox_renew --type pipeline --pipeline www.autobild.de
```

Renew a sandbox based an a property from Akamai
```
akamai staging sandbox_renew --type property --property-domain www.stage.autobild.de --property www.stage.autobild.de_ion
```

## stop and destroy a running sandbox
Remove a sandbox based on pipeline
```
akamai staging sandbox_stop --type pipeline --pipeline www.autobild.de
```

Remove a sandbox based on a property from Akamai
```
akamai staging sandbox_stop --type property --property-domain www.stage.autobild.de
```
