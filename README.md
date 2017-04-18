# Groovy Extension Module Sample

This project represents an extremely simple module extension.  The main point is to be 
concise, and not to show best practice.

The following demonstrates that ```groovysh``` will find an extension to the ```String``` class.  The shell appears to be checking in the file ```META-INF/services/org.codehaus.groovy.runtime.ExtensionModule``` for compiled code to use extensions.  In this case we only have the one module specified, ```SampleUtil```.
```
moduleName=Sample module extension
moduleVersion=1.0-test
extensionClasses=
staticExtensionClasses=SampleUtil
```


## Shell Session:
```
git clone  ...
cd shell-extension
groovyc SampleUtil
groovysh
$ groovysh
Groovy Shell (2.4.9, JVM: 1.8.0)
Type ':help' or ':h' for help.
------------------------------------------------------------------------------------------------------------------------------------
groovy:000> String.gotHere()
===> Hello, world.
groovy:000> 
```

# Reference:
* http://docs.groovy-lang.org/docs/groovy-2.3.8/html/documentation/#_extension_modules
