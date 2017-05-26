AutoFactory Annotations
=======================

A standalone packaging of the annotations from [Google's AutoFactory library][1].

(Inspired by JakeWharton's [AutoValueAnnotations][3])

When using AutoFactory with Gradle it is _highly_ inconvenient to specify the dependency both as
`annotationProcessor` and `provided`. Doing so leaks all of AutoFactory's annotation processor code and its
shaded dependencies into your classpath. It also causes issues with Proguard.
 This project allows you to only depend on the annotations
as `provided` and specify the processor only as an `annotationProcessor` dependency.


Download
--------

```groovy
annotationProcessor 'com.google.auto.factory:auto-factory:1.0-beta5'
provided 'com.episode6.hackit.auto.factory:auto-factory-annotations:0.0.1-SNAPSHOT'
```


License
-------

This project contains no code. See [AutoFactory's license][2] instead.







 [1]: https://github.com/google/auto/factory
 [2]: https://github.com/google/auto/blob/master/LICENSE.txt
 [3]: https://github.com/JakeWharton/AutoValueAnnotations