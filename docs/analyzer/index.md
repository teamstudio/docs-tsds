# Overview

You can test, debug and document your database design using Teamstudio Analyzer. Analyzer highlights functional dependencies within the design, verifies compliance with design standards, and uncovers compatibility issues before an upgrade. 

How does Analyzer work? 

* It reads the design of your Notes database or template.
* It analyzes this design.
* It builds a separate Notes database that represents the design. 

The new database contains a document for each design element (such as a form, view, subform or field). Each document contains the fields that represent the properties or attributes of the related design element. 

Analyzer can audit your design by testing it against a pre-defined set of criteria called filters. The Analyzer audit function identifies design elements that match the filter criteria and writes these audit results to an output database. This audit testing helps flag standards violations and potential performance problems for further review. 