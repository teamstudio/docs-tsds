# Troubleshooting Profiler

The following tips may help prevent or resolve issues you could encounter when running Profiler:

* Because of the way the Notes client performs caching, you should restart the Notes client before running Profiler.
* Line profiling is not available for code included from .lss files.
* Make sure the code you want to profile has not yet been loaded when you start Profiler. For example, if you want to profile the LotusScript code for a button, make sure that the form that the button is on is not open. Otherwise, Profiler will not recognize that the code is running.