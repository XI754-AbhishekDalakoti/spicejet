grunt-protractor-e2e-test
=========================
Sample code for starting up browser testing using protractor and grunt.

pre-requisite
=============
For running protractor tests, we need to install grunt-cli and protractor:

```
npm install -g grunt-cli
```

Above command will install grunt-cli for all users. You can choose if you just want for the current project using --save-dev command.

Navigate to your project directory and execute below command:

```
npm install protractor  --save-dev
```

Above command will install protractor in your project.


once these are installed, navigate to node_modules/grunt-protractor-runner/node_modules/protractor/bin you will see webdriver-manager, execute below command:

```
node webdriver-manager update
```

Above steps will selenium dependencies including webdriver which is required to run selenium tests. It will create a directory by name selenium inside under protractor directory and download chromedriver driver and selenium stand alone server based on protractor version.

running test
============

Now we can run test:

```
grunt test:e2e
```

Chrome browser will launch and test will execute.


results
=======

Results will look like as below:
```
Running "protractor:run" (protractor) task
[13:37:10] I/local - Starting selenium standalone server...
[13:37:10] I/launcher - Running 1 instances of WebDriver
[13:37:12] I/local - Selenium standalone server started at http://10.8.43.251:53019/wd/hub
Started
..


2 specs, 0 failures
Finished in 15.488 seconds
[13:37:30] I/local - Shutting down selenium standalone server.
[13:37:30] I/launcher - 0 instance(s) of WebDriver still running
[13:37:30] I/launcher - chrome #01 passed

Done, without errors.
```

ToDo
====
Adding API for page object access
