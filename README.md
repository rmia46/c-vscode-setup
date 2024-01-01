# c-vscode-setup

# Setting up VS-Code with GCC

## Setting up MinGW on Windows

1. **Download MinGW:** Download the mingw64 compiler from this [Github Repo](https://github.com/msys2/msys2-installer/releases) Choose the **"mingw-w64-install.exe"** file.

2. **Run the Installer:** Double-click the downloaded installer file and follow the on-screen instructions to run the MinGW-w64 installation wizard. Choose the installation directory (e.g., `C:\mingw-w64`) and select the desired components to install. Make sure to include the C and C++ compilers.

3. **Add MinGW to the PATH variable:** This step is very important. After installation, you need to add the MinGW directory to the system's PATH environment variable. This allows you to run MinGW commands from any location in the command prompt.

   - Open the Start menu and search for `Environment Variables.`
   - Select `Edit the system environment variables.`
   - In the `System Properties` window, click on the `Environment Variables` button.
   - In the `System Variables` section, select the `Path` variable and click the `Edit` button.
   - Add a new entry with the path to the MinGW `bin` directory (e.g., `C:\mingw-w64\mingw64\bin` or `C:\mingw-w64\mingw32\bin`).
   - Click `OK` to save the changes.

4. **Verify the Installation:** Open a new command prompt aka `cmd` window and type `g++ --version` to verify that the MinGW installation was successful. You should see the version information of the C++ compiler. Otherwise it will show an error. On that case follow the previous steps again carefully.

## Setting up Visual Studio Code

1. **Download and Install VS Code:** Visit the official [VS Code website](https://code.visualstudio.com) and download the installer for Windows. Run the installer and follow the on-screen instructions to install VS Code.

2. **Install the C/C++ Extension:** Launch VS Code and open the Extensions view by clicking on the square icon on the left sidebar or pressing `Ctrl+Shift+X`. Search for the **C/C++** extension by Microsoft and click the "Install" button. Once installed, click **Reload** to activate the extension.

3. **Install the Code Runner Extension:** In the Extensions view, search for the **Code Runner** extension by Jun Han and click the "Install" button. Again, click **Reload** to activate the extension.

4. **Enable Auto Save:** Open the VS Code settings by clicking on the gear icon in the lower-left corner and selecting **Settings**. In the Settings tab, search for `Auto Save` and select the option **After Delay**. Choose a suitable delay time or set it to **onFocusChange** to save files automatically whenever the focus is changed. You can achieve the same by activating auto-save from clicking `File` from the menubar.

5. **Configure Code Runner to Run in Terminal:** Hit `Ctrl+,` or manually open the vs-code setting from the gear-icon in the lower-left corner. Now on the settings tab, search for `@ext:formulahendry.code-runner` to access the `Code Runner` extension settings. Now scroll to find `Run in terminal` option and activate it.

That's it! You have successfully set up MinGW on Windows and configured Visual Studio Code with the necessary extensions. Now you can start writing and running C/C++ code in VS Code using MinGW as the compiler.

On most Linux Distributions gcc is installed by default. You just need to configure vs-code. Installing vs-code is also simple. Microsoft officially provides `.deb` and `.rpm` packages on their website. You can just download and install them directly. For those using `arch-linux` they can figure out themselves I guess. 
