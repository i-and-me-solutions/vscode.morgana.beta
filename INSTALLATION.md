# Installing the Morgana Beta Extension

The Morgana Extension consists of two components:

* **Morgana VS Code Extension** - The main extension that runs in Visual Studio Code
* **Morgana Backend** - A server component that runs on IBM i

While you can use the VS Code extension independently, some features (such as opening referenced files) require the Morgana Backend to be installed on your IBM i system for full functionality.

## Install VS Code Extension via VSIX file

To install the Morgana Beta extension in Visual Studio Code using a VSIX file, follow these steps:

1. **Get the VSIX File**
    - Contact us at [morgana@iandme.rocks](mailto:morgana@iandme.rocks) to request access to the VSIX file. We'll provide you with the download link or send the file directly.

2. **Open Visual Studio Code**
   - Launch Visual Studio Code on your computer.

3. **Access the Extensions View**
   - Click on the Extensions icon in the Activity Bar on the side of the VS Code window. Alternatively, you can open the Extensions view by pressing `Ctrl+Shift+X` (Windows/Linux) or `Cmd+Shift+X` (macOS).

4. **Install from VSIX**
   - Click on the `...` (More Actions) button in the top-right corner of the Extensions view.
   - Select `Install from VSIX...` from the dropdown menu.

5. **Locate the VSIX File**
   - In the file dialog that appears, navigate to the location where you saved the VSIX file.
   - Select the VSIX file and click `Open`.

6. **Wait for Installation**
   - VS Code will install the extension. Once the installation is complete, you will see a confirmation message.

7. **Reload VS Code (if required)**
   - Some extensions may require you to reload VS Code to activate them. If prompted, click the `Reload` button.

Your Morgana Beta extension is now installed and ready to use.

## Install Morgana Backend for IBM i

To install the Morgana Beta extension Backend for IBM i, follow these steps:

1. **Get the Savefile**
    - Contact us at [morgana@iandme.rocks](mailto:morgana@iandme.rocks) to request access to the Savefile for IBM i. We'll provide you with the download link or send the file directly.

2. **Transfer Savefile to your IBM i Partition**
   - Transfer the Savefile to your IBM i as you do it normally. If you never copied a Savefile to IBM i, please contact us at 
[morgana@iandme.rocks](mailto:morgana@iandme.rocks)

3. **Restore the Library to your IBM i Partition**
   - Sign On with a user that has enough rights to restore a Library. We suggest to use a SECOFR Profile in the Beta Phase.
   - Let's assume you restored the Savefile into your Savefile MORGANA in QGPL, then you simply can do a
   RSTLIB SAVLIB(MORGANA) DEV(*SAVF) SAVF(MORGANA) 

4. **Start the Backend Batch Job**
   - In Beta 1 we still use the ILE Open Source Framework ILEastic for communicating between the VS Code Add On and the IBM i Backend. Therefore you need to set a Port in the Frontend and also in Backend. In Beta 2 we will replace this way of communicating by the Code4i DB2 for i Communication path so you will not need any Ports.
   - Please be aware that your Firewall need to allow the communication to the Port on IBM i
   - The user which will be used to run the Batch Job need to have Access to all the sources and Objects you want to use withing Morgana Outline. For example if you have a RPG Programm in Lib "HUGO" and that uses Display Files in the same Lib and you want to open the source of the DSPF directly within Morgana Outline, the User which runs the Batch Job need to have the authority for Lib HUGO and all the Source Files you want to use. Because you already work with Code4i we expect that your user Profile has enough rights but be aware - if you are more than one developer in your company all developers will share that Batch Job in the Backend so it needs a user who maybe has access to different developer Libs.
   - Starting Morgana Backendservice can be like this:
   SBMJOB CMD(CALL PGM(MORGANA/STRMORGANA) PARM(('MORAPIBETA') ('44023') ('MORGANA') ('QINTER'))) JOB(MORAPIBETA) JOBQ(QINTER)     There are 4 Parameters to be passed to the STRMORGANA CL Programm:
   - PGMNAME --> which is MORAPIBETA
   - PORT --> which is the Portnumber you want to Morgana Backend to listen on your IBM i
   - PGMLIB --> which is the Library you installed Morgana Backend - normally it should be MORGANA
   - JOBQ --> The JobQ in which the Batch Job should be transferred so you can control where it will run
   If everything works you should see two entries in your WRKACTJOB Screen within the Subsystem you submitted the Job into
   <img width="876" height="51" alt="image" src="https://github.com/user-attachments/assets/52bda389-e437-4f16-b328-95114ab12483" />

5. **DONE**
   - If something doesn't work as expected please contact us at [morgana@iandme.rocks](mailto:morgana@iandme.rocks)
