# Roles

The plugin adds these roles automatically to resources. You cannot add these roles manually.

* zOSFileComponentProperties
* zOSFileImportProperties

### zOSFileComponentProperties


| Name | Type | Description | Reference |
| --- | --- | --- | --- |
| Default Shiplist | String | Input the content of a shiplist. When both shiplist content and shiplist file are specified, the shiplist content is used. | ${p:component/zOSFileComponentProperties/defaultShiplistContent} |
| Default Shiplist File | String | Specify the path to a default shiplist file on the host. | ${p:component/zOSFileComponentProperties/defaultShiplitFilePath} |
| Version Name Prefix | String | Specify a version name prefix. | ${p:component/zOSFileComponentProperties/versionNamePrefix} |

### zOSFileImportProperties


| Name | Type | Description |
| --- | --- | --- |
| Shiplist | String | Input the content of a shiplist. If left blank the default shiplist content is used. When both shiplist content and shiplist file are specified, the shiplist content is used. |
| Shiplist File | String | Specify a time stamp to include artifacts modified arfter this timestamp. Specify LASTVERSION to use the time stamp of the last version. If left blank, all artifacts in shiplist are included. |
| Version Name | String | Specify the version name. If left blank, a version name is generated based on the prefix and current time stamp. |



|          Back to ...          |                                |                                                                                 Latest Version                                                                                  | z/OS File Source Config |                   |                   |                   |                           |
|:-----------------------------:|:------------------------------:|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------:|:----------------------------------------:|:-----------------:|:-----------------:|:-----------------:|:-------------------------:|
| [All Plugins](../../index.md) | [Deploy Plugins](../README.md) | [8.1159269](https://raw.githubusercontent.com/UrbanCode/IBM-UCD-PLUGINS/main/files/zos-multi-generate-artifact-info/ucd-plugins-zos-multi-generate-artifact-info-9.1176022.zip) |           [Readme](README.md)            | [Steps](steps.md) | [Usage](usage.md) |[Roles](roles.md) |[Downloads](downloads.md) |Text
