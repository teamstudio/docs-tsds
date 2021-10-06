# Using Profiler Server

Install the Profiler Server on your Domino server so you can monitor the performance activity of a scheduled or Web agent.

Profiler Server uses the following databases on your server:

* Teamstudio/ProfilerConfig.nsf – Where you tell Profiler what to monitor.
* Teamstudio/ProfilerLog.nsf – Where Profiler keeps its results. 
 
!!! note
    Profiler is not intended to be used to monitor agents all of the time. Profiler creates a significant performance hit each time it is triggered by an agent. When not using Profiler, we recommend that you disable every agent in the Profiler Configuration database.