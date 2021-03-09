# Gradle Build with openshift s2i

steps:
 1. Add the build image. 

  -  oc import-image my-quarkus-s2i --confirm --from quay.io/quarkus/ubi-quarkus-native-s2i --all

 2. To build native :
 
   - oc new-app my-quarkus-s2i:21.0-java11~https://github.com/onlysumitg/gradle_s2i.git#main 

 3. to build jar:
   
   -  oc new-app my-quarkus-s2i:21.0-java11~https://github.com/onlysumitg/gradle_s2i.git#main --build-env BUILD_TYPE="jar"


Todo:
- make same setup for maven
