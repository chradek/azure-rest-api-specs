## Python

These settings apply only when `--python` is specified on the command line.

``` yaml $(python)
python:
  azure-arm: true
  license-header: MICROSOFT_MIT_NO_VERSION
  payload-flattening-threshold: 2
  package-name: azure-mgmt-eventhub
  clear-output-folder: true
  no-namespace-folders: true
```

### Python multi-api

Generate all API versions currently shipped for this package

```yaml $(python) && $(multiapi)
batch:
  - tag: package-2018-01-preview
  - tag: package-2017-04
  - tag: package-2015-08
```

### Tag: package-2018-01-preview and python

These settings apply only when `--tag=package-2018-01-preview --python` is specified on the command line.
Please also specify `--python-sdks-folder=<path to the root directory of your azure-sdk-for-python clone>`.

``` yaml $(tag) == 'package-2018-01-preview' && $(python)
python:
  namespace: azure.mgmt.eventhub.v2018_01_01_preview
  output-folder: $(python-sdks-folder)/azure-mgmt-eventhub/azure/mgmt/eventhub/v2018_01_01_preview
```

### Tag: package-2017-04 and python

These settings apply only when `--tag=package-2017-04 --python` is specified on the command line.
Please also specify `--python-sdks-folder=<path to the root directory of your azure-sdk-for-python clone>`.

``` yaml $(tag) == 'package-2017-04' && $(python)
python:
  namespace: azure.mgmt.eventhub.v2017_04_01
  output-folder: $(python-sdks-folder)/azure-mgmt-eventhub/azure/mgmt/eventhub/v2017_04_01
```

### Tag: package-2015-08 and python

These settings apply only when `--tag=package-2015-08 --python` is specified on the command line.
Please also specify `--python-sdks-folder=<path to the root directory of your azure-sdk-for-python clone>`.

``` yaml $(tag) == 'package-2015-08' && $(python)
python:
  namespace: azure.mgmt.eventhub.v2015_08_01
  output-folder: $(python-sdks-folder)/azure-mgmt-eventhub/azure/mgmt/eventhub/v2015_08_01
```
