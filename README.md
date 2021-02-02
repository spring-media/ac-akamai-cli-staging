# Akamai CLI: Domain Staging command

This repo is an command for Akamai CLI to staging given domains and to make it easy to handle sandbox with pipelines.

## Install
Installation this module via `akamai install`:
```
$ akamai install https://github.com/spring-media/ac-akamai-cli-staging.git
```

## Updating
To update to the latest version:
```
$ akamai update staging
```

## Get the lines for /etc/hosts of the domain(s) in the akamai staging network 
To run it:
```
$ akamai staging hosts www.akamai.com
$ akamai staging hosts www.akamai.com,www.akamai.de
```

## Attention
If you start a sandbox and there is no tls certificate found to use it will be created. This step will be imported the pem file of the certificate to MacOS Keychain. Please confirm this and enter yout password if you get the question for it.
This imported certificate will be used from Safari and Chrome.

## Use staging module to work with sandbox and pipeline
To create and run a sandbox for a defined domain and pipeline. The default pipeline environment is "stage":
```
akamai staging sandbox_start --type pipeline --pipeline www.autobild.de --pipeline-dir <local_dir_of_pipeline>
```

Renew a sandbox based on pipeline
```
akamai staging sandbox_renew --type pipeline --pipeline www.autobild.de
```

Remove a sandbox based on pipeline
```
akamai staging sandbox_stop --type pipeline --pipeline www.autobild.de
```

## Use staging module to work with sandbox and akamai property
To create and run a sandbox for a property from Akamai
```
akamai staging sandbox_start --type property --property www.stage.autobild.de_ion --property-domain www.stage.autobild.de
```

Renew a sandbox based an a property from Akamai
```
akamai staging sandbox_renew --type property --property-domain www.stage.autobild.de --property www.stage.autobild.de_ion
```

Remove a sandbox based on a property from Akamai
```
akamai staging sandbox_stop --type property --property-domain www.stage.autobild.de
```
