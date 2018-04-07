Example project to reproduce this issue https://discuss.gradle.org/t/correct-way-to-use-lombok-with-gradle-4-7-rc

Commands to copy-paste:

```
git clone git@github.com:nsiniakevich/gradle-4.7rc-lombok.git
cd gradle-4.7rc-lombok.git
./gradlew build -Dorg.gradle.warning.mode=all
```

Now we can verify that message below appears in terminal

>The following annotation processors were detected on the compile classpath: 'lombok.launch.AnnotationProcessorHider$AnnotationProcessor' and 'lombok.launch.AnnotationProcessorHider$ClaimingProcessor'. Detecting annotation processors on the compile classpath is deprecated and Gradle 5.0 will ignore them. Please add them to the annotation processor path instead. If you did not intend to use annotation processors, you can use the '-proc:none' compiler argument to ignore them.

---

This project was created from [start.spring.io](https://start.spring.io) with updated gradle wrapper to 4.7-rc-1 and updated build.gradle file.