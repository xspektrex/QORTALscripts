
<h1 align="center">
~ QORTector Scripts and how to's (Updated 11.19.23) ~
</h1>

<p>
Simple scripts and how to's to make tasks easier for users of the QORTectors and home built pi4's and linux.
The scripts herein are not be utilized on other Linux systems unless explicitly indicated in the list or images below this body of text.
</p>

```
    The stated scripts are applicable to other linux distros that are Qortal nodes only:
      - unintall_ui.sh
      - update_install_ui.sh
```
---

## Newcomers Start Here

1. Ensure `git` is installed via terminal with the command `git --version`
    - If no git version is listed simply install git via terminal with the command `sudo apt install git`

3. Download UI install/update and removal scripts to your home folder via terminal immediately after terminal load:
```
     wget https://raw.githubusercontent.com/xspektrex/QORTectorScripts/master/update_install_ui.sh && wget https://raw.githubusercontent.com/xspektrex/QORTectorScripts/master/uninstall_ui.sh
```

3. Download Qortal Core & Qortal-UI launchers to your home folder via terminal immediately after terminal load:
```
     wget https://raw.githubusercontent.com/xspektrex/QORTectorScripts/master/Launch_Core.sh && wget https://raw.githubusercontent.com/xspektrex/QORTectorScripts/master/Launch_UI.sh
```

4. Make the downloaded script/s executable:

    - via terminal immediately after load with  `chmod +x *.sh`

    - Via GUI with  `(Right-click -> Properties -> Permissions)` and check the "make executable" box.

6. Cut/paste Core & UI launchers to desktop

7. Now run the update_install or uninstall script/s via termianl immediately after load:
   ```
   sudo ./<script name with file extension> eg: sudo ./install_update_ui.sh
   ```

---

## Important Details (2023) Mark-II:

1. Since the nodesource nodejs install procedure has changed there are now 2 sets of scripts.

    ```
       - Post 2023 mark-II repo change scripts prefixed with nothing
       - Pre 2023 mark-II repo change scripts prefixed with "prc_njs_"
    ```

3.  Please utilize the appropriate procedural flow indicated below:
    - If doing a fresh install (Preferred)
        - Load terminal and ensure nodeJS is not already installed via APT, as it will not be a recent release, via the command below
           ```
               Sudo apt purge nodeJS
           ```
       - Load terminal and download/make executeable/run the `install_update_ui.sh` via the command below to install the qortal-ui via the updated method
         ```
              wget https://raw.githubusercontent.com/xspektrex/QORTectorScripts/master/install_update_ui.sh && chmod +x *.sh && ./install_update_ui.sh
         ```
      
    - If updating for the first time since the scripts noted at the top of this page were updated (11.19.2023)
        - Load terminal and download/make executeable/run the `prc_njs_2023_unintall_ui.sh` script via the command below to remove the existing qortal-ui install
             ```
              wget https://raw.githubusercontent.com/xspektrex/QORTectorScripts/master/prc_njs_2023_uninstall_ui.sh && chmod +x *.sh && ./prc_njs_2023_uninstall_ui.sh
             ```
        - Load terminal and download/make executebale/run the `update_install_ui.sh` script via the command below to install the qortal-ui via the updated method
             ```
              wget https://raw.githubusercontent.com/xspektrex/QORTectorScripts/master/update_install_ui.sh && chmod +x *.sh && ./update_install_ui.sh
             ```

## <strike>Important Details (2023) Mark-I (Deprecated):

1. Since the qortal-ui repo has been restructured there are now 2 sets of scripts.

```
    - Post 2023 repo change scripts prefixed with nothing
    - Pre 2023 repo change scripts prefixed with "prc2023"
```

2.  If a clean install is preferred, and it is suggested, the following procedural flow must be followed based on the indicated situation
    - If doing a fresh install 
        - Ensure nodeJS is not already installed via APT as it will not be a recent release
           ```
               Sudo apt purge nodeJS
           ```
      
    - If updating for the first time since the repo re-orginization
        - Ensure nodeJS is not already installed via APT as it will not be a recent release
              ```
                Sudo apt purge nodeJS
              ```
        - Run the `prc2023unintall_ui.sh` script to remove the qortal-ui install that was previously the normal installer
        - Run the `update_install_ui.sh` script to install the qortal-ui
        
3. Finish up by re-installing curl
   
           sudo apt install curl 


    
# Important Details (2022) (Deprecated):

1. Since the UI repo has changed from "UI" to "qortal-ui" there are now 2 sets of scripts.

```
    - Pre repo change prefixed with "prc"
    - Post repo change prefixed with nothing
```
    
2.  If a clean install is preferred, and it is suggested, the pre repo change uninstaller should be utilized before utilizing the post repo change installer.

