# DataBox

> see https://aka.ms/autorest

This is the AutoRest configuration file for DataBox.



---
## Getting Started
To build the SDK for DataBox, simply [Install AutoRest](https://aka.ms/autorest/install) and in this folder, run:

> `autorest`

To see additional help and options, run:

> `autorest --help`
---

## Configuration



### Basic Information
These are the global settings for the DataBox API.

``` yaml
openapi-type: arm

input-file:
- Microsoft.DataBox\preview\2018-01-01\databox.json
directive:
  - suppress:
    - R2016 #to suppress (PatchBodyParametersSchema/R2016/RPCViolation)
    - R2062 #to suppress (XmsResourceInPutResponse/R2062/RPCViolation)
```
---
# Code Generation


## Swagger to SDK

This section describes what SDK should be generated by the automatic system.
This is not used by Autorest itself.

``` yaml $(swagger-to-sdk)
swagger-to-sdk:
  - repo: azure-sdk-for-go
  - repo: azure-sdk-for-node
```


## C#

These settings apply only when `--csharp` is specified on the command line.
Please also specify `--csharp-sdks-folder=<path to "SDKs" directory of your azure-sdk-for-net clone>`.

``` yaml $(csharp)
csharp:
  azure-arm: true
  license-header: MICROSOFT_MIT_NO_VERSION
  namespace: Microsoft.Azure.Management.DataBox
  output-folder: $(csharp-sdks-folder)/DataBox/Management.DataBox/Generated
  clear-output-folder: true
```


## Go

These settings apply only when `--go` is specified on the command line.

``` yaml $(go)
go:
  license-header: MICROSOFT_APACHE_NO_VERSION
  namespace: databox
  clear-output-folder: true
```

### Go multi-api

``` yaml $(go) && $(multiapi)
```

### Tag: package-2017-06 and go

Please also specify `--go-sdk-folder=<path to the root directory of your azure-sdk-for-go clone>`.

``` yaml $(go)
output-folder: $(go-sdk-folder)/services/databox/mgmt/2018-01-01/databox
```


## Java

These settings apply only when `--java` is specified on the command line.
Please also specify `--azure-libraries-for-java-folder=<path to the root directory of your azure-libraries-for-java clone>`.

``` yaml $(java)
java:
  azure-arm: true
  fluent: true
  namespace: com.microsoft.azure.management.databox
  license-header: MICROSOFT_MIT_NO_CODEGEN
  payload-flattening-threshold: 1
  output-folder: $(azure-libraries-for-java-folder)/databox
```
