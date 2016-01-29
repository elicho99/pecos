Custom applications
====================

Pecos can be customized for specific applications.  Python scripts can be added 
to initialize data and add data from models.  Additional quality control tests 
can be added by inheriting from the PerformanceMonitoring class.

PV system monitoring
---------------------
For PV systems, the translation dictionary can be used to group data
according to the system architecture, which can include multiple strings and modules.
The time filter can be defined based on sun position and system location.
The data objects used in Pecos are compatible with pvlib, which can be used to model PV 
systems (https://github.com/pvlib/pvlib-python).
Pecos also includes a function to read Campbell Scientific ascii file format.

Pecos includes a PV system example, **pv_driver.py**, in the examples/pv directory.  
The example combines application specific functions in **pv_application.py**, 
which computes the sun position using pvlib, 
generates custom graphics and performance metrics. 

Performance metrics
---------------------
The performance metrics file, created by Pecos, can be used for additional 
analysis.

Pecos includes a performance metrics example (based on PV metrics), **metrics_driver.py**, in the examples/metrics directory.
