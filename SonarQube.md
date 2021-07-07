# SonarQube Plugin

`SonarQube` is an open source platform to perform automatic reviews with static analysis of code to detect bugs, code smells and security vulnerabilities on 25+ programming languages including Java, C#, JavaScript, TypeScript, C/C++, COBOL and more. SonarQube is the only product on the market that supports a leak approach as a practice to code quality.



#### Install SonarQube IntelliJ Plugin
* In your IDE go to `Settings -> Plugins`
* Search for `‘sonarqube’` and install the plugin

![install](https://github.com/CharmiTrambadiya/Documents/blob/master/images/installplugin.PNG)


#### Setting up SonarQube plugin
* In IntelliJ go to `File -> Settings -> Other Settings -> SonarQube`
* Add details about the sonar server here. The plugin will use this to download the    quality profile/analyzers etc.
* This plugin executes the analysis in preview mode where no data is pushed to the     server.

![install](https://github.com/CharmiTrambadiya/Documents/blob/master/images/server.PNG)

![install](https://github.com/CharmiTrambadiya/Documents/blob/master/images/settings.PNG)


#### Run the analysis
* click on the `Code -> Inspect Code`
* In the "Inspection Scope" dialog, select File and also you can select the Whole project also.

![install](https://github.com/CharmiTrambadiya/Documents/blob/master/images/inspectcode.PNG)

* The plugin will run the preview analysis and display the results in the inspection tab.

![install](https://github.com/CharmiTrambadiya/Documents/blob/master/images/result.PNG)
