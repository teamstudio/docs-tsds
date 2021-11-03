# Overview

You are often faced with the difficult task of examining a database design to ensure it can meet some, unique, criteria. Examples of this are:

* Is the design compatible with the next release of Notes?
* Can the design be moved to another environment?
* Does it meet company standards?

Analyzer's analysis function helps with these decisions by extensively documenting the attributes and contents of a design, and by providing views that help answer many of these questions. Sometimes, however, you must examine a combination of elements and their attributes to properly answer a question.

The audit function can help by letting you define requirements and then test the design of the database or template to make sure it meets the requirements. Many of these requirements are reusable, such as standards or common coding errors. Others will have a unique temporary nature, such as a special change request or compatibility issues raised by upgrades to a new version of Notes. Auditor includes some predefined tests that give you a head start on defining typical tests such as locating the following:

* Common coding errors
* Potential performance problems
* Violations of typical organizational standards
* Potential application upgrade problems
* Potential Web or O/S compatibility problems