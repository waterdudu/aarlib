# A demo to upload android project to private maven repo


open ```local.properties```, replace your own ```sdk.dir```

```
sdk.dir=/Users/dudu/Documents/programs/android-sdk-macosx
```


change your private maven repository url, username and password in ```gradle.properties```
```
repositoryUsername=MAVEN_ANDROID_REPO_USERNAME
repositoryPassword=MAVEN_ANDROID_REPO_PASSWORD
repositoryUrl=http://mvn.corp.mycompany.com/nexus/content/repositories/android-repo
```

when you have new version, you can change version info in ```gradle.properties```
```
VERSION_NAME=0.0.4
GROUP=com.x.aarlib101
```

call 
```
gradle uploadArchives
```

Now your aarlib101 library project will be uploaded to private maven repository
