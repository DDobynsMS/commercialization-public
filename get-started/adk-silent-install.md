---
author: alhopper
Description: Instructions on how to install the ADK silently
MSHAttr: 'PreferredLib:/library/windows/hardware'
title: Windows ADK silent install
ms.author: alhopper
ms.date: 05/02/2017
ms.topic: article
ms.prod: windows-hardware
ms.technology: windows-oem
---
# Windows ADK silent install

If you have a scenario where you need to silently install the Windows ADK, you can install using the command line.

Make sure that your PC remains connected to the Internet while ADK Setup is running. ADK Setup downloads installation packages from the Internet while it runs.

## Install the Windows ADK by using the command line

1. Download adksetup.exe to your PC.
2. Open a Command Prompt as administrator.
3. In the Command Prompt window, change to the directory that contains adksetup.exe.

```PowerShell
    cd %userprofile%\downloads
```

1. Install the ADK. Use /quiet for silent installation. Use /features to specify features. For example, install Deployment Tools and Windows PE silently:

```PowerShell
    adksetup.exe /quiet /features OptionId.DeploymentTools OptionId.WindowsPreinstallationEnvironment
```
## Related topics

[ADKSetup Command-Line Syntax](https://technet.microsoft.com/en-us/library/dn621910.aspx).