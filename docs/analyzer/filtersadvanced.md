# Auditor Filters for Advanced Users

The Filter wizard creates a validation formula which is a standard Notes formula. Advanced users may avoid the limitations of the wizard by manually completing the validation formula field.

You should build your filters a step at a time to ensure that each part works correctly before you add more to it. Since Auditor requires that you use the design of the Analyzer template, you must use fields or alias names from **ivesdean.ntf**.

!!! note
    Analyzer Auditor processes documents in the analysis database. This means that any time you reference a field name it must be a valid field on a form referenced by the **Apply To** value.  
    If you plan to write validation formulas manually, we recommend that you familiarize yourself with the design of the Analyzer template (ivesdean.ntf). A good starting point is to analyze the Analyzer template. 
    
Generally, filter validation formulas are standard Notes formulas. Analyzer extends these formulas for special purposes with advanced functions. 