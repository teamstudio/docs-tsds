# Release Notes

Edition 35 is a feature release of the Teamstudio Notes tools. The primary new feature is support for the HCL  12.0.2 64 bit Designer client. All of the Teamstudio tools except for Profiler have been updated to run in a 64 bit environment. Due to internal implementation details, Profiler will continue to be fully supported on 32 bit Notes clients, but will not be available on 64 bit.  

!!! Note
    There are now separate installers for 32 and 64 bit Notes. You should choose the installer that matches your **Notes** version, not your Windows version. So if you are running 32 bit Notes on 64 bit Windows, you need the 32 bit installer.  The installer will verify your Notes version and will not allow you to install a version of the tools that does not match your version of Notes.

In addition to 64 bit support, we have significantly optimized the performance of the CIAO! UI, especially over slow connections. There are major performance improvements both in launching CIAO and in updating the UI after a checkin/out operation.
 
## Fix List
### 35.0.0
184300373 Fixed crash in 'Open in Library Pane' using Design Manager  
184331236 Display 'Modified (initially)' rather than 'Modified (in this file)' in the CIAO UI  
184331249 Minor CIAO UI performance improvements  
184331185 Optimize character set conversions in the CIAO UI  
184444716 Fix rare Analzyer Audit hang with TMSIncludeParent rules
