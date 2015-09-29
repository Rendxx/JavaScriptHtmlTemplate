# JavaScriptHtmlTemplate
A Visual Studio template for JavaScript / HTML / Less. With Npm / Bower / Gulp for environment setup.

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

# Gulp Task
Gulp is used to process JavaScript and LESS files.
See **gulpfile.js** for details.
  
# Setup
1. Download the template zip file
2. Move the zip file to template directory.
   *the*