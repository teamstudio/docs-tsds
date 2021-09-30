# Installing on the Notes Client

## Introduction
Client-based modules include:

* Analyzer
* CIAO! Client Edition
* Configurator
* Delta
* Design Manager
* Profiler
* Undo
* Validator

You install client tools on each developer's workstation.

If you are using them, you should first install the CIAO! and Profiler server components on a Notes/Domino server. See [Install Server-based Modules](server.md) for details.

## Windows Installer
Beginning with Edition 32, the Notes Tools installer utilizes Windows Installer. This offers a more conventional installation experience than earlier versions and replaces the Widget Installers and the beta MSI installers from E31.1.

## Installation
* Verify that the system you are installing on meets the system requirements in the [Before You Begin](before.md) section.
* Download the Notes Tools installer from the [Download Page](https://www.teamstudio.com/client-tools-download-page).
* Close and exit all Notes client processes (Notes, Designer, Admin, etc.).
* Launch the downloaded "Notes Tools.exe" installer, and follow the instructions in the installation wizard.

The installation wizard will allow you to confirm the location of the Notes client install, and choose which tools in the suite to install.

The installation utilizes artifacts from the Notes client installation and can encounter issues if Notes has been moved or upgraded in certain ways. If you experience errors during installation, contact techsupport@teamstudio.com for guidance on how to resolve installation issues.

!!! note
    If you previously installed a beta release with the same major and minor version number as the
    version you are installing, you must remove the existing install first, via the Windows Control
    Panel's "Add or Remove Programs" feature.  
    If you installed the tools using the E31.1 beta MSI installers, we recommend removing the tools
    via the Windows Control Panel before installing E32. The E32 installer will upgrade your tools
    in any case, but it is not able to remove the old Control Panel entries. In all other cases,
    the E32 installer should be able to upgrade your existing installation.
    
## Installation Changes in E32
* The tools are no longer installed using widgets. The installer will attempt to remove previous widgets as part of the upgrade process.
* The client tools are no longer installed to the Notes program directory. They are now installed, by default, to C:\Program Files (x86)\Teamstudio\Notes Tools\bin and this directory is added to the current user's PATH. No files are installed to the Notes program directory.
  <div class="admonition">
    <p class="admonition-title">Note</p>
    <p>If you are upgrading from an older version of the tools, the E32 installer needs to remove
    any old Teamstudio files from the Notes program directory. If you are running Notes from a file
    server, you will need write access to that directory for the initial E32 install. Subsequent
    upgrades will no longer write to the Notes program directory.</p>
  </div>
* A single installer now handles the installation of all products. This means that all products from E32 onwards must be upgraded together. So when you upgrade to E32.1, for example, you cannot upgrade just Teamstudio Analyzer and leave Teamstudio Configurator at E32. This only applies to E32 and above - it is possible to retain, say, E31.1 of Teamstudio Analyzer and install E32 of Teamstudio Configurator. While rare, if you need to downgrade to an older version, you will need to uninstall all products and then reinstall the older version.
* It is no longer necessary to remove older versions before upgrading. The installer will automatically remove previous versions as part of the installation process.
* All installation directories are now configurable. The installer will attempt to find your Notes program directory, data directory and notes.ini location but you can modify them if you have a complex configuration that the installer does not correctly recognize. You can also change the directory in which the Teamstudio tools are installed, although this is not recommended.