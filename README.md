[![Build Status](https://travis-ci.org/tonysneed/Demo.VSCode.TypeScript.svg?branch=master)](https://travis-ci.org/tonysneed/Demo.VSCode.TypeScript)
# Demo: Sample Visual Studio Code project for TypeScript

*NOTE: This generator is designed to work only on Mac OS X or Linux. 
To work on Windows, a number of issues will need to be addressed, 
including differences in file paths.*

1. You should first install the following **extensions** for Visual Studio Code.
  - [VS Code JSHint](https://marketplace.visualstudio.com/items?itemName=dbaeumer.jshint): ```jshint```
  - [VS Code TSHint](https://marketplace.visualstudio.com/items?itemName=eg2.tslint): ```tslint```
  - [Editor Config for VS Code](https://marketplace.visualstudio.com/items?itemName=chrisdias.vscodeEditorConfig): ```editorconfig```
    + To install an extension, type Cmd+P to diplay the Command Palette, then type ext and press Enter.
    + Type the extension keyword shown above and press Enter to install.
    + ```editorconfig``` will bring up two extensions, so just install *Editor Config for VS Code*.

2. Open a Terminal at the project root and execute the following scripts.

  - Install npm packages. A **node_modules** folder will be created with 
    required packages.

    ```
    npm run init
    ```
    
  - Compile TypeScript files. A **dist** folder will be created with files
    generated by the TypeScript compiler, including source maps and type defs.
  
    ```
    npm run compile
    ```

3. Make sure you can **debug** TypeScript source files and tests.

  - Select `greeter.ts` in `src\greeter\greeter.ts`
  - Click the Debug icon in VS Code.
  - Select *Debug Current TypeScript File* dropdown and press **F5** to launch
    the debugger and break on the first line.
  - Then select `greeter.spec.ts` and set a breakpoint.
  - Select *Debug Current TypeScript Test* dropdown and press **F5** to launch
    the debugger and stop at the breakpoint.
    
4. Launch the **build** and **test** tasks from within VS Code.

  - Press **Cmd+Shift+B** to build.
  - Press **Cmd+Shift+T** to run tests and see result in the Output window.

5. Next you can execute **gulp** tasks from the Terminal.

  - Note that gulp commands can also be run from within VS Code, pressing
    **Cmd+P** and typing **task**, then typing part of the task name.

  - Show available gulp commands.
  
    ```
    gulp
    ```

  - Run jasmine tests using **karma**.
  
    ```
    gulp tests-run
    ```

  - Run jasmine tests using **karma** with a **watch**.
    After running, make a change to `greeter.spec.ts` so that it fails.
  
    ```
    gulp tests-watch
    ```

  - Serve jasmine tests in the **browser**.
    After running, make a change to `greeter.ts` so that it fails.
  
    ```
    gulp tests-serve
    ```

6. TypeScript files and tests may be added to the **src** directory, 
   either at the src root or in nested subdirectories.
   
