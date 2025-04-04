# CS502_project
# Remote SSH to UW-Madison CSL Workspace through VSCode

This document provides step-by-step instructions on how to set up the VS Code Remote SSH extension wiht your UW-Madison Computer Sciences Lab (CSL) account. This is a helpful tool for your C oriented classes where your development enviornment is required to be on a linux machine for the proper compliation requirements. This tool will enable you to access all of those necessary linux resources from an SSH client built directly into your VS Code on your peresonal machine.

## Prerequisites

Before you begin, make sure you have the following:

- CSL Username. If you don't know your CSL username, navigate to this website [CSL UW-Madison](https://csl.cs.wisc.edu), then click at "MY CS ACCOUNT". Follow instructions. Your CSL username should be under "CS Username"  
- A working installation of Visual Studio Code (VS Code) can be downloaded through the [VS Code Download](code.visualstudio.com)
- Navigate to your extensions tab of VSCode on the left hand tool bar. Search for "Remote - SSH" and download the extension onto your machine. Further instructions below.

## Steps

1. Open VS Code on your local machine.

2. Install the "Remote - SSH" extension by following these steps:
    - Click on the Extensions view icon in the sidebar (or press `Ctrl+Shift+X`).
    - Search for "Remote - SSH" in the Extensions view search bar.
    - Click on the "Remote - SSH" extension by Microsoft and click the "Install" button.

3. Once the extension is installed, naviagte to settings. Check the boxes for "Remote.SSH: Lockfiles In Tmp" and "Remote.SSH: Show Login Terminal"

4. You will notice you have a new tab in the toolbar on the left hand side of your VS Code window. Click on the tab that corresponds to your Remote SSH tool.

5. We will now configure your CSL account as a target for the SSH client. This will enable you to just click on the target and sign in on future sessions.
    - Click the Configure icon at the right of SSH Targets
    - Select the first SSH configuration file to edit
    - Add the following snippet to your configuration file, making sure to add in your CSL username in the User field

``` 
Host CSL
    HostName best-linux.cs.wisc.edu
    User your-CSL-username
```

## Connecting

Connecting to your CSL account is as simple as clicking your new entry under SSH Targets in the Remote Explorer tab on your VS Code window and typing in your password.

## Troubleshooting

If you encounter any issues during the setup process, refer to the official documentation of the VS Code Remote SSH extension for troubleshooting steps.

The terminal tab on the bottom tab on your VS Code will show the commands being issues to and from the VS Code sesison in the attempt to SSH. Any issues encountered during conneciton will be apparent here.


## Conclusion

By following the steps outlined in this document, you should be able to successfully set up the VS Code Remote SSH extension and start working with your remote machine from within VS Code.
