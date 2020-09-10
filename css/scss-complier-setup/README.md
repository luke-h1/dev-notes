## SCSS node workflow


  * npm init 
  * npm i -D sass 
  * create two directories: css & scss 
  * link your css stylesheet in your html as this is where the scss will be compiled 
  ```
  mkdir css 
  mkdir scss 
  ``` 
  * create an npm script for compliling sass into css with the following command: 
  ```
  sass --watch scss/styles.scss css/styles.css
  ```
  * the above script watches the scss/styles.scss for changes and compiles the sass into css/styles.css
  * another option would be to use the vs code extension live-sass-compiler