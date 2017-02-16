# gradle-docker-plugin-issue-347

this repo demonstrates how to reproduce issue https://github.com/bmuschko/gradle-docker-plugin/issues/347

To reproduce the bug, just call
```
./gradlew version
```

When you remove the plugin `org.asciidoctor.gradle.asciidoctor` from the plugins list the build works.
So this bug seems to be caused by defining multiple plugins, even though the asciidoctor plugin is not applied!!!
