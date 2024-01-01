# c-vscode-setup

# Setting up MinGW on Windows and Visual Studio Code

## Setting up MinGW on Windows

1. **Download MinGW:** Download https://github.com/msys2/msys2-installer/releases download the MinGW-w64 installer for your system architecture (32-bit or 64-bit). Choose the "mingw-w64-install.exe" file.

2. **Run the Installer:** Double-click the downloaded installer file and follow the on-screen instructions to run the MinGW-w64 installation wizard. Choose the installation directory (e.g., `C:\mingw-w64`) and select the desired components to install. Make sure to include the C and C++ compilers.

3. **Add MinGW to the PATH variable:** After installation, you need to add the MinGW directory to the system's PATH environment variable. This allows you to run MinGW commands from any location in the command prompt.

   - Open the Start menu and search for "Environment Variables."
   - Select "Edit the system environment variables."
   - In the "System Properties" window, click on the "Environment Variables" button.
   - In the "System Variables" section, select the "Path" variable and click the "Edit" button.
   - Add a new entry with the path to the MinGW `bin` directory (e.g., `C:\mingw-w64\mingw64\bin` or `C:\mingw-w64\mingw32\bin`).
   - Click "OK" to save the changes.

4. **Verify the Installation:** Open a new command prompt window and type `g++ --version` to verify that the MinGW installation was successful. You should see the version information of the C++ compiler.

## Setting up Visual Studio Code

1. **Download and Install VS Code:** Visit the official [VS Code website](https://code.visualstudio.com) and download the installer for Windows. Run the installer and follow the on-screen instructions to install VS Code.

2. **Install the C/C++ Extension:** Launch VS Code and open the Extensions view by clicking on the square icon on the left sidebar or pressing `Ctrl+Shift+X`. Search for the **C/C++** extension by Microsoft and click the "Install" button. Once installed, click **Reload** to activate the extension.

3. **Install the Code Runner Extension:** In the Extensions view, search for the **Code Runner** extension by Jun Han and click the "Install" button. Again, click **Reload** to activate the extension.

4. **Enable Auto Save:** Open the VS Code settings by clicking on the gear icon in the lower-left corner and selecting **Settings**. In the Settings tab, search for **Auto Save** and select the option **After Delay**. Choose a suitable delay time or set it to **onFocusChange** to save files automatically whenever the focus is changed.

5. **Configure Code Runner to Run in Terminal:** Open the Command Palette by pressing `Ctrl+Shift+P` and type **Preferences: Open Settings (JSON)** to open the `settings.json` file. Add the following configuration to enable running code in the terminal:

   ````json
   "code-runner.runInTerminal": true
   ```

   Save the file.

That's it! You have successfully set up MinGW on Windows and configured Visual Studio Code with the necessary extensions. Now you can start writing and runni ng C/C++ code in VS Code using MinGW as the compiler.

Feel free to customize the formatting and styling further to suit your needs.
