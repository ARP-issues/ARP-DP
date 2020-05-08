### **Description**

This repository includes the mapping relationships between dangerous permissions and Android APIs (API-DP mappings) corresponding to API level 23 to API level 29. The permission specifications are obtained by mining the Javadoc of Android SDK. More importantly, this repository also provides the differences of such mappings across different Android versions. 

We hope that app developers should pay special attention to the evolution of permission specifications and adapt their apps accordingly to avoid incompatibility issues.

### **Mining API-DP mappings**

From Android 6.0 (API level 23), Google formally documents permission specifications in two ways: 

- using Java annotation `@requiresPermission` to associate APIs with permissions 
- using `@link android.Manifest.permission# `to describe an API's required permissions.

To infer API-DP mappings, we developed a tool APMiner (http://arp-issues.github.io/) to analyze the Javadoc of the Android SDK.

### **Evolution of API-DP Mappings** 

In this repository, we provide three types of permission specification changes between different Android versions:

- the addition/deletion of permission-protected APIs; 
- the addition/deletion of dangerous permissions;
- the changes in the mapping relations between APIs and permissions. 