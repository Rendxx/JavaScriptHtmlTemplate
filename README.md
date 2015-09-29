# JavaScriptHtmlTemplate
A Visual Studio template for JavaScript / HTML / Less. With Npm / Bower / Gulp for environment setup.

*Latest Version Download: [Simple Webpage with JS and LESS v1.0.0][Latest]*

# Structure
- **src/**   
  Directory of source files.  
  **src/js/**   
  Directory of **JavaScript** source files.  
  **src/less/**   
  Directory of **LESS** source files.  

- **wwwroot/**   
  Directory of processed files.  
  **wwwroot/js/**   
  Directory of bundled and minimized **JavaScript** files.  
  **wwwroot/css/**   
  Directory of **Css** files, bundled and created from LESS files.   
  **wwwroot/lib/**   
  Directory of 3rd-party files, copied from Bower directory.  
  **wwwroot/images/**   
  Directory of images.  

- **index.html**  
  HTML file

- **bundle.json**  
  Use to set bundle / minimization / processing of JavaScript and LESS files.  
  **bower.json**  
  Bower file  
  **package.json**  
  NPM file  
  **gulpfile.js**  
  Gulp file  
  
# Setup
1. Download the template zip file

2. Move the zip file to Visual Studio custom template directory.  
    Path: *\\My Documents\\Visual Studio Version\\Templates\\ProjectTemplates\\*  
    More information: [How to: Locate and Organize Project and Item Templates][Templates Directory] 

3. Open Visual Studio.  
    Click **File** > **New** > **Project** > **Installed** > **JavaScript**  
    Select **Simple Webpage with JS and LESS**

4. Open and save **package.json** to install npm packages  
    Open and save **bower.json** to install bower packages  
    Open and save **gulpfile.json** to setup gulp task

5. Run gulp task **_copyBower** to copy bower packages  
    Run gulp task **js** to process JavaScript files  
    Run gulp task **less** to process Less files  
    Run gulp task **_watch** if you want to setup automatic processing on editing JavaScript/Less files  

6. Now you are all set. Open **index.html** in browser to see the default page.

# Gulp Task
Gulp is used to process JavaScript and LESS files.  
[More information about Gulp][Gulp]

- **js**  
  Process and combine JavaScript files listed in *bundle.json*, minimized files will be created as well.  
  All processed files will be put in *wwwroot\\js\\*

- **less**  
  Process and combine Less files listed in *bundle.json*  
  All processed files will be put in *wwwroot\\less\\*

- **\_watch**  
  Setup automatic processing on editing JavaScript/Less files.  
  This task will run automatically when this project opens after gulp set.

- **\_copyBower**  
  Copy selected files from Bower packages. It only need to be ran once after installing Bower packages.

- **\_cleanLib**  
  Clear the 3rd-party directory. Called by task **\_copyBower**.

# Usage
1. **Modifying JavaScript/LESS Files**  
    All JavaScript/LESS files should be placed in the corresponding directories in *src/*.

2. **Add Bundle**  
    All JavaScript/LESS files should be listed in *bundle.json*. Otherwise it will be ignored by processing tasks.

3. **Add Link in HTML File**  
    To use JavaScript/LESS files in HTML file, add links to the processed files in *wwwroot\\*.


[Templates Directory]: https://msdn.microsoft.com/en-us/library/y3kkate1.aspx "How to: Locate and Organize Project and Item Templates"
[Gulp]: https://github.com/gulpjs/gulp/blob/master/docs/getting-started.md "Gulp Doc"
[Latest]: https://github.com/Rendxx/JavaScriptHtmlTemplate/releases/tag/1.0.0 "Download Page"