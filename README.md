![metronode](http://www.metronode.org/img/logo/metronode-96x96.png) MetroArgs
==================

Support for Build Variables in Universal Apps <br />
Part of the [MetroNode](http://www.nuget.org/packages/MetroNode) toolset.

***

#How to Setup
1. Install the [MetroArgs](http://www.nuget.org/packages/MetroArgs) NuGet package to your project
2. Load up the configuration file in your JS:
``` Javascript
 WinJS.xhr({ url: ".metroargs.json" }).then(function (respObj) {
        var parsedObject = JSON.parse(respObj.responseText);
        console.log(parsedObject.Configuration);
    });
```

#Source Control
The configuration file is generated at runtime and stored in a file called `.metroargs.json`. 
Consider adding wildcard match `.*` to your exclusion file for Git/SVN/HG.


#Additional Arguments
Please contribute to the project by appending your desired MSBuild arguments to the packages build definition.
The desired goal is to export all build-time arguments into an NConf Compatible configuration file for usage at runtime.
