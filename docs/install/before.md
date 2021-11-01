# Before You Begin

## Review System Requirements
Teamstudio Client has the following system requirements:

* Windows Vista, Windows 7, Windows 8 and Windows 10 versions supported by Notes on Intel platforms
  <div class="admonition note">
    <p class="admonition-title">Note</p>
    <p>Microsoft has discontinued support for Windows XP and Windows Server 2003. Teamstudio Tools are not supported on these platforms. Please contact your account manager if you have questions about running our tools on Windows XP or Windows Server 2003.</p>
  </div>
* Notes, in versions currently supported by HCL.
  <div class="admonition note">
    <p class="admonition-title">Note</p>
    <p>Teamstudio Notes Tools typically work without issue on earlier versions of Notes, and technical support is available for customers on legacy versions of Notes. Teamstudio may not, however, be able to provide fixes for issues that are specific to unsupported versions of Notes. For more information on installing Teamstudio tools on earlier versions of Notes, contact <a href="mailto:techsupport@teamstudio.com">techsupport@teamstudio.com</a>.</p>
    <p>To verify your version of Notes is supported by HCL check HCL's <a href="https://support.hcltechsw.com/csm?id=kb_article&sysparm_article=KB0068850&sys_kb_id=d9e7f06e1be51cd0f37655352a4bcb4d">Support Lifecycle</a></p>
  </div>
* Approximately 50 MB of hard disk drive space
* Sufficient RAM to run HCL Lotus Notes
* Sufficient Windows permissions to install software on your local machine.

Teamstudio CIAO! Server has the following system requirements:

* Windows Server versions as supported by your version of Domino server
* 32bit & 64bit Domino Server versions as currently supported by HCL

Teamstudio Profiler Server has the following system requirements:

* Windows Server versions as supported by your version of Domino server
* 32bit Domino Server versions as currently supported by HCL


!!! Note
    The Analyzer Filters database included in this release is **deanfltr.ntf**.
    
    If you are using **deanfltr.ntf** and have changed it in any way, you must save it to another file name before you install this release. Otherwise, you will lose your changes or customizations.
    
    To upgrade your filters database:
    
    1. Make a copy of your current Analyzer Filters Database (**deanfltr.nsf** or **deanfltr.ntf**).
    2. Create a new database (**File > Database > New**) and name it **deanfltr.nsf** and then select the Analyzer Filters Template from the template box.
    3. Click Yes when Notes asks you if you want to overwrite the existing one. (It’s ok, you’ve made a copy.)
    4. Copy all your custom filters from your old database into this new database.