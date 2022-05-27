
WinRS Agent Install - Steps
===========================

# Steps



### Steps




 



### Process steps in the WinRS Agent Install plug-in


* [WinRS Agent Install](#winrs_agent_install)





### WinRS Agent Install


Install agent to remote machine using WinRS


Before you can run this step, you must 
configure the target system as described in [Installing agents on Windows through 
WinRS](http://www-01.ibm.com/support/knowledgecenter/SS4GSP_6.1.2/com.ibm.udeploy.install.doc/topics/agent_install_winrs.html)
 in the product documentation.




| Name | Type | Description | Required |
| --- | --- | --- | --- |
| Agent Host | 
String | The hostname or IP address of the machine to install an agent to. | Yes |
| Agent Name | String | The name that
 the agent should show up as in IBM UCD. | Yes |
| Installation Directory | String | The directory that the agent should
 be installed to. | Yes |
| Java Home | String | The directory that java is pre-installed to. | Yes |
| Mutual 
Authentication | Boolean | Use mutual authentication? | Yes |
| Password | Password | The password of the machine to 
install an agent to. | Yes |
| Proxy Host | String | The hostname of any proxy between the agent and IBM UCD server | No
 |
| Proxy Port | String | The JMS Port of any proxy between the agent and IBM UCD server | No |
| Server Host | String 
| The hostname of the IBM UCD server | Yes |
| Server Port | String | The JMS Port the server listens on | Yes |
| 
Temporary Directory | String | The directory that should be used for a temporary workspace. | Yes |
| Username | String 
| The username of the machine to install an agent to. | Yes |





|Back to ...||Latest Version|WinRS Agent Install |||
| :---: | :---: | :---: | :---: | :---: | :---: |
|[All Plugins](../../index.md)|[Deploy Plugins](../README.md)|[12.1131558]()|[Readme](README.md)|[Overview](overview.md)|[Downloads](downloads.md)|