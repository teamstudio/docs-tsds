# Install Server-Based Modules

Optionally, you can install CIAO! and Profiler Server Editions onto each Domino server.

| Server Tool | Why Install? |
| --- | --- |
| CIAO! Server | Provides additional features, for example, preventing design changes made by any process or by someone other than the developer who checked the design element out. |
| Profiler Server | Tests the performance activity of a scheduled agent or a web agent. |

## Windows Installation Procedure

Before you begin, make sure of the following:

* You have purchased a license for each server you want to install on. CIAO! and/or Profiler Server Editions are licensed per Domino server.

### To install CIAO! Server Edition

1. Copy the files:
    1. Put nhkciao.dll into the server's exe directory (same as nserver.exe)
    2. Put ciaologf.ntf and ciao.ntf into the data directory.
2. From a notes client create the following databases on the server using the templates on that server.  
    * CIAO\CIAOConfig.nsf (Template: Teamstudio CIAO! Configuration)  
    * CIAO\CIAOLog.nsf (Template: Teamstudio CIAO! Log File)
3. Add the serial key:  
    1. Create a file called teamstudio.ini in the data directory of the server.  
    2. Add the following lines:
    ```
    [CIAO]  
    HKCIAOKey=xxxxx-xxxxx-xxxxx,xx-xxxxx  
    CIAOConfigDb=CIAO\CIAOConfig.nsf  
    ```
   replacing the xxx with your license followed by a comma and your serial number.
4. Edit your notes.ini to add/modify the following line:
```
NSF_HOOKS=hkciao
```
5. Restart the Domino server.  
   If you see lines similar to this:
```   
CIAO Server Hook started - (SERVER). (HKCIAO Edition 33 build xxxxx)
CIAO Server Hook: Using Configuration File: CIAO\CIAOConfig.nsf
```
   then you know that CIAO Server Edition is running.  

### To install Profiler Server Edition
1. Copy the files:
    1. Put nhkprofile.dll into the server's exe directory (same as nserver.exe)
    2. Put profile.ntf and tmslogs.ntf into the data directory.
2. From a Notes client create the following database on the server using the template on that server.
    * Teamstudio\ProfilerConfig.nsf (Template: Teamstudio Profiler Configuration)
3. Add the serial key as follows:
    1. Create a file called teamstudio.ini in the data directory of the server.
    2. Add the following lines:
    ```
    [Profiler]
    HKPROFKey=xxxxx-xxxxx-xxxxx,xx-xxxxx
    ProfilerServerConfig=Teamstudio\ProfilerConfig.nsf
    ```
    replacing the xxx with your license followed by a comma and your serial number.
4. Edit your notes.ini to add/modify the following line:
```
NSF_HOOKS=hkprofile
```
5. Restart the Domino server.
    If you see lines like the following, then you know that Profiler Server Edition is running:
```
(namgr) - Profiler Server Hook started. (HKPROFILE Edition 33 build xxxxx)
Profiler Server Hook: Using Configuration File: Teamstudio\ProfilerConfig.nsf
```