# GenAI Summary Release-OpenAI - Usage

To use the GenAI Summary Release–OpenAI plug-in, the plug-in must be loaded and an instance created before you can configure the plug-in integration. You can define configuration properties in the user interface.

## Integration

### Integration type

The GenAI Summary Release–OpenAI plug-in is an end-point type plug-in. It analyzes the issues which are ongoing to Release after latest prod Release.

### Prerequisites
1. IBM DevOps Velocity 5.0.8 or later
2. Release Summary docker image (GenAI Summary Release–OpenAI plug-in)


### Offline Integration

The table in the Configuration properties section describe the properties used to define the integration.

1. Pull release summary docker image.
2. In IBM DevOps Velocity, click **Settings > Integrations > Available**.
2. Click **Load Plugin**, and enter `[RELEASE SUMMARY IMAGE NAME]:[LATEST_TAG]`. For example `ucv-ext-release-summary-openai:1.0.1`.
3. On the Add Integration page enter values for the fields used to configure the integration and define communication.
4. Click **Add**.

### Online Integration

The table in the Configuration properties section describe the properties used to define the integration.

To install the plug-in, perform the following steps:

1. In IBM DevOps Velocity, click **Settings > Integrations > Available**.
2. In the Action column for the GenAI Summary Release-OpenAI plug-in, click **Install**.

To integrate the plug-in, perform the following steps:

1. In IBM DevOps Velocity, click **Settings > Integrations > Installed**.
2. In the Action column for the GenAI Summary Release-OpenAI plug-in, click **Add Integration**.
3. On the Add Integration page enter values for the fields used to configure the integration and define communication.
4. Click **Add**.

### LLM Service Configuration
Provide the following plug-in configuration options:

- **OpenAI API Key**: API key to authenticate and use with the OpenAI service

## Invoking the plug-in

The plug-in is invoked when you generate the Release Readiness Report after integrating with the Handlebar reporter plug-in. The data from the GenAI Summary Release–OpenAI plug-in is displayed in a section called Release Summary within the Release Readiness Report.

The plug-in exposes the following endpoints:
1. `/reporting-consumer/pluginEndpoint/[INTEGRATION ID]/generate` This endpoint starts the generation of release summary. It expect to provide as part of the body the following parameter:
  - `vsmid` id of the value stream to generate the summary
  - `releaseid` id of the release to generate the summary
  - `currentStageName` pipeline stage containing the release candidate
  - `targetStageName` targeted release stage
  - `allVersions` if true, it will generated the summary considering work items of all versions associated with the release 
  
  The following is a sample curl command:

    curl -i -X POST \
        -H "Content-Type:application/json" \
        -d \
        '{
            "vsmid" : "6641e92d735e31769cb2f7cc",
            "releaseid" : "669548dc6d0a6b58e6a0add4",
            "targetStageName" : "PROD",
            "currentStageName" : "DEV"
        }' \
    'https://.../reporting-consumer/pluginEndpoint/669e12a21e0e8a001b70ec35/generate'
    
  
**Note**: Change the `669e12a21e0e8a001b70ec35` with the integration id of the created integration.

2. `../reporting-consumer/pluginEndpoint/[INTEGRATION ID]/emulate` This endpoint is provided for just testing purposes. It emulates the generation of the summary and can be used to test the integration of release summary plug-in with IBM DevOps velocity. Expected schema is 
 - `vsmid` id of the value stream to generate the summary
  - `releaseid` id of the release to generate the summary
  - `currentStageName` pipeline stage containing the release candidate
  - `targetStageName` targeted release stage
  - `allVersions` if true, it will generated the summary considering work items af all versions associated with the release 
  
The following is a sample curl command:
    
    curl -i -X POST \
        -H "Content-Type:application/json" \
        -d \
        '{
            "vsmid" : "6641e92d735e31769cb2f7cc",
            "releaseid" : "669548dc6d0a6b58e6a0add4",
            "targetStageName" : "PROD",
            "currentStageName" : "DEV"
            "releaseid" : "6641e4ce818a54c626097ad4"
        }' \
    'https://.../reporting-consumer/pluginEndpoint/669e12a21e0e8a001b70ec35/emulate'

**Note**: Change the `669e12a21e0e8a001b70ec35` with the integration id of the created integration.

## Exploring the summary
Generated summary will be stored as a field of the `release` document. The following graphql query can be use to search and retrive a generated summary.

    query releaseEventById(\$release_id : ID\!){
                releaseEventById(_id : \$release_id){
    				summary
    				lastSummaryOn
                }
        }

## Configuration Properties

The following tables describe the properties used to configure the integration. Each table contains the field name when using the user interface and the property name when using a JSON file.

|Name|	Type|	Description|	Required|	Property Name|
|----|----|----|----|----|
|Integration Name	|string	|The name for plug-in integration	|Yes	|name|
|LLM-Drop-Down|	array	|LLM provider	|Yes	|llmDropdown|
|OPENAI_APIKEY|	string	|The Api-key for OPENAI|	Yes	|OPENAI_APIKEY|


|Back to ...||Latest Version|GenAI Summary Release-OpenAI|||
| :---: | :---: | :---: | :---: | :---: | :---: |
|[All Plugins](../../index.md)|[Velocity Plugins](../README.md)|[1.0.1](https://hub.docker.com/r/urbancode/ucv-ext-release-summary-openai/tags)|[Readme](README.md)|[Overview](overview.md)|[Downloads](downloads.md)|