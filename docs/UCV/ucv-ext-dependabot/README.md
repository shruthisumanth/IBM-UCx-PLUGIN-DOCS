
# GitHub Dependabot

- The GitHub Dependabot plug-in scans known GitHub repositories and pulls security alerts into UrbanCode Velocity. This vulnerability information is available as various metrics and charts in the metrics bar and dashboard. In addition, you can leverage these values in your pipeline for automated gates and deployments. 
- The GitHub Dependabot leverage the existing GitHub plug-in to scan and link against known repositories. It is highly recommend that you install and configure the existing GitHub plug-in before you install the GitHub Dependabot plug-in. 
- GitHub Dependabot Alerts should be enabled for the GitHub repository. Automated pull requests generated by Dependabot will be also visible in the Value Stream. 
- This is a scheduled event plug-in and runs on a timed interval. If data ever gets out of sync, please leverage the Last Initial Sync utility.

|Back to ...||Latest Version|GitHub Dependabot |||
| :---: | :---: | :---: | :---: | :---: | :---: |
|[All Plugins](../../index.md)|[Velocity Plugins](../README.md)|[1.0.2](https://raw.githubusercontent.com/UrbanCode/IBM-UCV-PLUGINS/main/files/ucv-ext-dependabot/ucv-ext-dependabot:1.0.2.tar.7z.001)|[Overview](overview.md)|[Usage](usage.md)|[Downloads](downloads.md)|