# Orphaned Agent Data Notes

This test scans a database to identify agent data notes that are no longer being referenced by an agent. Agent data notes are design elements created and used by agents when they run. Over time, some databases accumulate hundreds of these elements, increasing the size of the database. Since most orphaned agent data notes are no longer attached to an agent, they will never be deleted. There is no easy way to remove them since they do not show up in Designer.

The following is an example of a Validator report showing orphaned agents.
<figure markdown="1">
  ![Error](img/agentdata.png)
</figure>

This report provides only the common information described earlier. 

## To remove orphaned agent data notes in a report
* Click the **Remove Agent Data** button at the top of the window to remove the orphaned agent data notes referenced in this report.

## To remove all orphaned agent data notes
1. Go to the view called **Orphan Agent Data Notes**.
2. Click the **Remove Agent Data** button at the top of the window to remove all the orphaned agent data notes.
 
