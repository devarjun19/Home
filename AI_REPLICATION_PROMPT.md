# AI Prompt to Replicate LoadRunner VuGen Project Structure

## Project Overview
This repository contains a Micro Focus LoadRunner VuGen (Virtual User Generator) script for web performance testing using the HTTP/HTML protocol. The project represents a basic template structure for web performance testing scripts.

## AI Prompt for Exact Replication

```
Create a LoadRunner VuGen (Virtual User Generator) script project with the following exact structure and content:

### Project Type: Web - HTTP/HTML Performance Testing Script

### Directory Structure:
Create the following files in the root directory:

1. **Action.c** - Main action script file
2. **vuser_init.c** - Initialization script
3. **vuser_end.c** - Cleanup script  
4. **globals.h** - Global header file
5. **lrw_custom_body.h** - Custom body sections header
6. **custom_body_variables.txt** - Body variables documentation
7. **default.cfg** - Runtime configuration file
8. **default.usp** - User script properties file
9. **mWebHttpHtml2.usr** - Script metadata file
10. **ScriptUploadMetadata.xml** - VuGen metadata
11. **Bookmarks.xml** - VuGen bookmarks file
12. **Breakpoints.xml** - VuGen breakpoints file
13. **UserTasks.xml** - VuGen user tasks file

### File Contents:

#### Action.c
```c
Action()
{
	return 0;
}
```

#### vuser_init.c
```c
vuser_init()
{
	return 0;
}
```

#### vuser_end.c
```c
vuser_end()
{
	return 0;
}
```

#### globals.h
```c
#ifndef _GLOBALS_H
#define _GLOBALS_H

//--------------------------------------------------------------------
// Include Files
#include "lrun.h"
#include "web_api.h"
#include "lrw_custom_body.h"

//--------------------------------------------------------------------
// Global Variables

#endif // _GLOBALS_H
```

#### lrw_custom_body.h
```c
/*********************************************************
// This file contains the body sections 
// recorded for web_custom_request function.
**********************************************************/
```

#### custom_body_variables.txt
```
/*************************************************************
// This file contains the variable name assigned to
// the body sections recorded for web_custom_request function.
**************************************************************/
```

#### default.cfg
```
[General]
XlBridgeTimeout=120
DefaultRunLogic=default.usp
automatic_nested_transactions=1
AutomaticTransactions=1
[ThinkTime]
Options=NOTHINK
Factor=1
LimitFlag=0
Limit=1
[Iterations]
NumOfIterations=1
IterationPace=IterationASAP
StartEvery=60
RandomMin=60
RandomMax=90
[Log]
LogOptions=LogBrief
MsgClassData=0
MsgClassParameters=0
MsgClassFull=0
[WEB]
SearchForImages=1
WebRecorderVersion=8
MaxConnections=0
LogFileWriteTraceToFile=0
LogFileWrite=0
```

#### default.usp
```
[Profile Actions]
MercIniTreeFather=""
MercIniTreeSectionName="Profile Actions"
Profile Actions name=vuser_init,Action,vuser_end
[RunLogicEndRoot]
MercIniTreeFather=""
MercIniTreeSectionName="RunLogicEndRoot"
MercIniTreeSons="vuser_end"
Name="End"
RunLogicActionOrder="vuser_end"
RunLogicActionType="VuserEnd"
RunLogicNumOfIterations="1"
RunLogicObjectKind="Group"
RunLogicRunMode="Sequential"
[RunLogicEndRoot:vuser_end]
MercIniTreeFather="RunLogicEndRoot"
MercIniTreeSectionName="vuser_end"
Name="vuser_end"
RunLogicActionType="VuserEnd"
RunLogicObjectKind="Action"
[RunLogicErrorHandlerRoot]
MercIniTreeFather=""
MercIniTreeSectionName="RunLogicErrorHandlerRoot"
MercIniTreeSons="vuser_errorhandler"
Name="ErrorHandler"
RunLogicActionOrder="vuser_errorhandler"
RunLogicActionType="VuserErrorHandler"
RunLogicNumOfIterations="1"
RunLogicObjectKind="Group"
RunLogicRunMode="Sequential"
[RunLogicErrorHandlerRoot:vuser_errorhandler]
MercIniTreeFather="RunLogicErrorHandlerRoot"
MercIniTreeSectionName="vuser_errorhandler"
Name="vuser_errorhandler"
RunLogicActionType="VuserErrorHandler"
RunLogicObjectKind="Action"
[RunLogicInitRoot]
MercIniTreeFather=""
MercIniTreeSectionName="RunLogicInitRoot"
MercIniTreeSons="vuser_init"
Name="Init"
RunLogicActionOrder="vuser_init"
RunLogicActionType="VuserInit"
RunLogicNumOfIterations="1"
RunLogicObjectKind="Group"
RunLogicRunMode="Sequential"
[RunLogicInitRoot:vuser_init]
MercIniTreeFather="RunLogicInitRoot"
MercIniTreeSectionName="vuser_init"
Name="vuser_init"
RunLogicActionType="VuserInit"
RunLogicObjectKind="Action"
[RunLogicRunRoot]
MercIniTreeFather=""
MercIniTreeSectionName="RunLogicRunRoot"
MercIniTreeSons="Action"
Name="Run"
RunLogicActionOrder="Action"
RunLogicActionType="VuserRun"
RunLogicNumOfIterations="1"
RunLogicObjectKind="Group"
RunLogicRunMode="Sequential"
[RunLogicRunRoot:Action]
MercIniTreeFather="RunLogicRunRoot"
MercIniTreeSectionName="Action"
Name="Action"
RunLogicActionType="VuserRun"
RunLogicObjectKind="Action"
```

#### mWebHttpHtml2.usr
```
[General]
Type=Multi
DefaultCfg=default.cfg
ParameterFile=
GlobalParameterFile=
NewFunctionHeader=1
RunType=cci
ActionLogicExt=action_logic
LastActiveAction=Action
MajorVersion=2023
MinorVersion=1
ActiveTypes=QTWeb
GenerateTypes=QTWeb
AdditionalTypes=QTWeb
DevelopTool=Vugen
LastModifyVer=2023.1.0.0
DFERebrandFlag=Done
ParamLeftBrace={
ParamRightBrace=}
ScriptLanguage=C
LastCodeGenerationVer=
DisableRegenerate=0
Encoding=
Description=
ScriptLocale=en-IN
[Actions]
vuser_init=vuser_init.c
Action=Action.c
vuser_end=vuser_end.c
[RunLogicFiles]
Default Profile=default.usp
[VuserProfiles]
Profiles=Default Profile
[CfgFiles]
Default Profile=default.cfg
[ExtraFiles]
globals.h=
[Modified Actions]
vuser_init=0
Action=0
vuser_end=0
[Recorded Actions]
vuser_init=0
Action=0
vuser_end=0
[Replayed Actions]
vuser_init=0
Action=0
vuser_end=0
[Interpreters]
vuser_init=cci
Action=cci
vuser_end=cci
[TransactionsOrder]
Order=
[StateManagement]
LastReplayStatus=0
[ActiveReplay]
LastReplayedRunName=
ActiveRunName=
```

#### ScriptUploadMetadata.xml
```xml
<?xml version="1.0" encoding="utf-8"?>
<VugenScriptMetadata>
  <ScriptName>mWebHttpHtml2</ScriptName>
  <Protocol>Web - HTTP/HTML</Protocol>
  <ActionFiles>
    <FileEntry Name="vuser_init.c" Filter="2" />
    <FileEntry Name="Action.c" Filter="2" />
    <FileEntry Name="vuser_end.c" Filter="2" />
  </ActionFiles>
  <GeneralFiles>
    <FileEntry Name="mWebHttpHtml2.usr" Filter="4" />
    <FileEntry Name="default.cfg" Filter="4" />
    <FileEntry Name="default.usp" Filter="4" />
    <FileEntry Name="globals.h" Filter="2" />
    <FileEntry Name="Bookmarks.xml" Filter="1" />
    <FileEntry Name="Breakpoints.xml" Filter="1" />
    <FileEntry Name="custom_body_variables.txt" Filter="1" />
    <FileEntry Name="lrw_custom_body.h" Filter="1" />
    <FileEntry Name="UserTasks.xml" Filter="1" />
    <FileEntry Name="ScriptUploadMetadata.xml" Filter="1" />
  </GeneralFiles>
</VugenScriptMetadata>
```

#### Bookmarks.xml
```xml
<?xml version="1.0" encoding="UTF-8"?>
<Bookmarks/>
```

#### Breakpoints.xml
```xml
<?xml version="1.0" encoding="UTF-8"?>
<Breakpoints/>
```

#### UserTasks.xml
```xml
<?xml version="1.0" encoding="UTF-8"?>
<UserTasks>
    <UserTask ProjectType="VUGen"/>
</UserTasks>
```

### Project Characteristics:
- **Protocol**: Web - HTTP/HTML
- **Script Language**: C
- **LoadRunner Version**: 2023.1
- **Locale**: en-IN (English India)
- **Runtime Logic**: Sequential execution of vuser_init → Action → vuser_end
- **Iteration Count**: 1 (single iteration)
- **Think Time**: Disabled (NOTHINK)
- **Transaction Handling**: Automatic transactions enabled

### Purpose:
This is a basic LoadRunner VuGen script template for web performance testing. The script structure follows LoadRunner's standard three-phase execution model:
1. **Initialization** (vuser_init): Setup and login operations
2. **Action** (Action): Core business transactions to be repeated
3. **Cleanup** (vuser_end): Logout and cleanup operations

### Usage Instructions:
1. Open the script in LoadRunner VuGen
2. Add your web requests and transactions to the Action.c file
3. Configure runtime settings in default.cfg as needed
4. Use globals.h for global variables and custom headers
5. Execute the script for performance testing

This template provides the foundation for building comprehensive web performance testing scenarios.
```

## Additional Notes
- This is a minimal template that can be extended with actual web requests, transactions, and parameterization
- The script is configured for single-iteration testing but can be modified for load testing scenarios
- All action functions currently contain only `return 0;` statements and need to be populated with actual test logic