# WxSocketAdapter

This Socket Adapter project covers two demands of advanced Integration Server users and developers:
1. Demoing how to develop a custom coded on-premise Intgeration Server adapter.
2. Providing a light-weight way to connect low level devices and applications into the world of Integration Server.

This adapter deploys 3 ways of conneting to the Integration Server it is running on:

* TCP/IP client connectivity
* TCP/IP server connectivity
* Serial communication connectivity

A detailed sample presentation of the functionality providing screen shots can be viewed under Software AG's TECHCommunity (see link below).

# Prerequisits

* SAG's Integration Server (IS) or Microservices Runtime (MSR) version 10.5 or later is installed on your local machine.
* SAG's Designer (DES) - with perspective "Service Development" enabled - version 10.5 or later is installed on your local machine.
* At least the following packages are installed and enabled on the local IS:
    * WmRoot
    * Default
    * WmART
    * WmPublic
* You applied the latest fixes for IS, MSR, and DES.
* You know where to find the following jars and pathes on your local machine:
    * gf.jakarta.resource.jar (usually in common\lib\glassfish)
    * wm-isclient.jar (usually in common\lib)
    * jSerialComm-2.5.3.jar (usually in WxSocketAdapter\code\jars\static)
    * wm-isserver.jar (usually in IntegrationServer\lib)
    * WmART\code\classes (usually pointing to IntegrationServer\...\packages\WmART\code\classes)
    * wmart.jar (usually in IntegrationServer\...\packages\WmART\code\jars\)
* To see immediate results coming from the socktes, make sure you can receive messages with your Integration Server. So, if you are not connected to an UM, make sure your "webMethods Messaging Settings" of your IS is **"IS_LOCAL_CONNECTION"** (use "Change Default Connection Alias" to do so). 


# Installation

1. Clone this project into a local temporary directory
2. Copy the subdirectory "WxSocketAdapter" below directory "webmethods-integrationserver-wxsocketadapter" into your IS package directory, e.g. for MSR: c:\softwareag\IntegrationServer\packages.
4. Under ...\packages\WxsocketAdapter\code create a directory "src" or make sure it exists and move the subdirectories ...\packages\WxsocketAdapter\com and ...\packages\WxsocketAdapter\wm into the new subdirectory src or make sure it's populated with these subdirectories.
3. Open DES, switch to "Java" perspective and import the WxSocketAdapter project from IS package directory (Eclipse->file->import->General->Existing Projects Into Workspace).
4. You should see now a list of "missing required libraies".
5. Resolve these errors by running "Configure Build Path ..." for this project by adding the external jars and class folders.
6. After all errors are resolved the adapter is ready to use. **Please restart your IS/MSR**.




## 3rd Party License
The following 3rd party libraries are used within the adapter:

* jSerialComm-2.5.3.jar - please find license agreements under: https://github.com/Fazecast/jSerialComm
__________________
For more information you can Ask a Question in the [TECHcommunity Forums](http://tech.forums.softwareag.com/techjforum/forums/list.page?product=webmethods).

You can find additional information in the [Software AG TECHcommunity](http://techcommunity.softwareag.com/home/-/product/name/webmethods).
_________________
