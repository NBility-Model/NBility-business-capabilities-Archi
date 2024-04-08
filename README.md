# NBility-business-capabilities-Archi-Dutch

This repo contains NBility-business-capabilities model version 2.1 in Dutch and Archi format. The model is built using Archi. 

# View 
The model can be viewed [here without the need to install Archi](https://nbility-model.github.io/NBility-business-capabilities-Archi/).

# Edit  
To contribute to the LF Energy Archimate models you need [Archi](https://www.archimatetool.com/). 

# Step-by-step user guide for Archi

## Setting up and configuring Archi and the plug-in

### Installing Archi

1. Download and install the latest version of Archi from https://www.archimatetool.com/download/

### Download and install the coArchi plug-in

1. Download the most recent version of **coArchi** plug-in zip file from the [Archi plugins page](https://www.archimatetool.com/plugins/).

2. In Archi, select "Manage Plug-ins..." from the main Help menu. From the Plug-ins Manager window, select "Install New..." and select the **coArchi** plug-in zip file. You may need to restart Archi to activate the plug-in. Please ensure the plug-in version supports the installed version of Archi.

![coArchi-manage-plugins](https://github.com/NBility-Model/.github/blob/main/images/manage%20plug-ins.PNG)

![coArchi-manage-plugins-window](https://github.com/NBility-Model/.github/blob/main/images/manage%20plug-ins%20part%202.PNG)

3. If your plug-in installation was successful, the [**Collaboration**] menu item should be visible appear on the application menu in Archi after restarting Archi.

![coArchi-collaborate](https://github.com/NBility-Model/.github/blob/main/images/Collaboration.PNG)

## Preparing your Github account to configure Archi integration

1. Log onto your GitHub Account at [GitHub.com](github.com) or create a GitHub account at [GitHub.com](github.com)
2. To configure Archi for Github integration you would need to create a Personal Access Token (PAT) from your user account.  For a detailed overview of the process you can visit https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/creating-a-personal-access-token

Alternatively, you can follow the steps below:

### Create a Github Personal Access Token (PAT)

1. Select [**Settings**] from your account menu (look for the avatar at the right-top of the page)
   
![coArchi-github-settings](https://github.com/NBility-Model/.github/blob/main/images/Settings.PNG)

2. Select [**Developer settings**] from the menu on the left-hand of the page

![coArchi-github-developer-settings](https://github.com/NBility-Model/.github/blob/main/images/Developer%20settings.PNG)
   
3. Select [**Personal access tokens**] and then [**Tokens (classic)**]
4. Select [**Generate new token**] and then [**Generate new token (classic)**]
5. Enter your token name, set the token expiry and select the [**repo**] scope for the token
   
![coArchi-new-token](https://github.com/NBility-Model/.github/blob/main/images/New_personal_access_token.PNG)   

7. Click [**Generate token**]
8. Copy the token from the screen and store it securely for configuration purposes.  **IMPORTANT**: YOU CANNOT RETRIEVE THE TOKEN AFTER IT HAS BEEN GENERATED AND DISPLAYED ON THIS PAGE.  IF YOU LOOSE IT YOU WILL NEED TO GENERATE A NEW TOKEN.

![coArchi-personal-access-token](https://github.com/NBility-Model/.github/blob/main/images/New_personal_access_token%20part%202.PNG)


### Import the model into Archi from Github

Once you have configured Archi and coArchi, and generated your Github Personal Access Token (PAT) you will be able to import the Nbility model into archi.

1. In Archi, select [**Import Remote Model to Workspace**] from **Collaboration** menu.  You may need to provide Archi a master password to unlock this feature. **IMPORTANT**: YOU CANNOT RETRIEVE THE MASTER PASSWORD AFTERWARDS. IF YOU LOOSE IT YOU MAY WILL NEED TO REINSTALL ARCHI.

![coArchi-add-remote-model](https://github.com/NBility-Model/.github/blob/main/images/Add%20remote%20model.PNG)

2. In the **Add Remote Model** modal, provide the following information:

| Field       | Description |
| ----------- | ----------- |
| URL         | The full web URL of the repo: https://github.com/username/reponame.git |
| User Name   | Your Github user name |
| Password    | The Github Personal Access Token (PAT) you generated earlier |

It is possible that you could use your GitHub credentials as-is in the screen.  However, it is recommended that you enable 2FA on your Github account to protect access to the repo.  In this case you will only be able to log onto Github from Archi using the Github Personal Access Token (PAT).

To obtain the repo URL, you can copy of from the **Clone** address:

![coArchi-clone](https://github.com/NBility-Model/.github/blob/main/images/Clone%20address.PNG)

### Navigating the UI

1. In Archi, select [**Toggle Collaboration Workspace**] and [**Toggle Branches View**] from the **Collaboration** menu.  The Workspace and Branch windows will be docked within Archi.  Archi/coArchi supports repository branches.

![coArchi-navigate-ui](https://github.com/NBility-Model/.github/blob/main/images/Archi%20UI.PNG)

The Collaboration Workspace is used to navigate between different models and individual branches checked out while the Branches View provide the ability to manipulate branches within the selected model. 

### Refresh model

**It is important to refresh the model from Github prior to making any changes to avoid overwriting upstream changes made since the local repo copy was pulled from the server**.  Regular refreshes also help to keep local repo copies updated with changes made to the upstream repository. 

1. To refresh your local copy of the model, open the model / branch from the Collaboration Workspace and select [**Refresh Model**] from the **Collaboration** application menu.

![coArchi-refresh-model](https://github.com/NBility-Model/.github/blob/main/images/Refresh%20model%20part%202.PNG)

Alternatively, you can - in archi - select [**Toggle Collaboration Workspace**] from the **Collaboration** application menu and refresh Model there.

![coArchi-refresh-model-alternative](https://github.com/NBility-Model/.github/blob/main/images/Refresh%20model.PNG)

## Branching

To protect the integrity of the main branch and avoid overwriting updates from oneanother, it is recommended to create a branch for each new piece of work.  Branches could be named by initials, date or subdomain.  Branches can be created either through the coArchi plugin or online on Github.

![coArchi-add-branch]()

[**Add branch**] will create a local branch while [**Add branch and checkout**] will create the local branch and set it as the active branch.  Neither of these actions will create the upstream branch (on Github server).

![coArchi-switch-branch]()

### Committing changes

By committing changes you create a local snapshot of the repository into a single package.  **This does not upload the changes to the upstream branch, but create a local packaged copy**.  To commit your latest changes, select [**Commit changes**] from the Collaboration menu.

![coArchi-commit]()

### Publishing changes

The final step is to publish the committed package back to the repository.  This will insert the last committed package into the upstream branch.

### Merge

On regular intervals all committed and published branches need to be merged into the main branch which will trickle down into all subsequent branches.

## Further reading

For more information on the mechanics and command line (CLI) operations, you can read the following documents:

https://docs.github.com/en/get-started/using-git/about-git

https://git-scm.com/docs/gittutorial

# License
This project is licensed Creative Commons Attribution 4.0 International Public License (CC-BY-4.0) - see [LICENSE](LICENSE) for details.

# Contributing
Please read [CONTRIBUTING.md] for details on the process for submitting pull requests to us.

# Contact
Please read [SUPPORT.md] for how to connect and get into contact with the NBility-business-capabilities model project
